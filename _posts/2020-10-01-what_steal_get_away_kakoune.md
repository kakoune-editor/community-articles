---
title: What you could steal from the Kakoune code editor right now, and get away with it
author: Frank Lenormand
author-handle: lenormf
license: CC BY-SA 4.0
---

[Kakoune](https://kakoune.org/) is a (fairly) young modal code editor
that has matured for as long and as well as a good red wine. It places
multiple-selections, operability and interactivity at the heart of its
distinctive characteristics. It provides users with an efficient and
comfortable text editing experience — but that's not what this article
is about.

Now 8 years old at the time of writing, Kakoune has gone through several
iterations that removed a dependency here, optimised a core feature there,
even factorised entire parts of its codebase! And as any long-term user
will tell you, it's easy to take all that good stuff for granted.

So here it is. I'm stopping time for a couple minutes, and listing in
this article a few things that the Kakoune project does well in several
dimensions. Some are technical, but the rest should hopefully be easily
adaptable to other projects (whether they are code editors or not), and
generic enough to be adopted seamlessly.

Now why does the title of this piece mention stealing? Read on, that's item
number one.

From its licensing model
------------------------

If something doesn't belong to anybody, is it stealing if you take it for
yourself? What if it belongs equally to everybody?

Fortunately we don't need to solve that problem: Kakoune is a public domain
project. Which means that anyone is free to do anything they want with the
source code of the editor, no questions asked.

This has several advantages:

- the tool can be shipped with any distribution or suite, regardless of
  licensing
- users can modify the code (to fix bugs, add new features or tweak already
  existing ones etc.) and publish it (or compiled binaries) without worrying
  about attribution
- it lifts some weight of responsibility of the maintainer for the whole
  project, which anyone can re-brand or heavily modify to their liking

Users don't like paying for tools, and when they are free and open-source,
I'd argue that they turn out to be more useful (with several iterations,
over time) in the end if they place no limits on what users are allowed to
do with the code.

I'm not in favour of abolishing licenses, I think it would be more
productive for everyone if specialised tools were in the public
domain. In fact, the Kakoune project *is* licensed, under the
[terms](https://choosealicense.com/licenses/unlicense/) of the
[UNLICENSE](https://unlicense.org/), in order to avoid conflicts with
jurisdictions that don't recognise the *public domain* model.

As for the small riddle above, that's a tough one, bordering on the
philosophical, but since we're talking about replicating data, we can easily
break out of that paradox: copying is not stealing.

From its code
-------------

New comers like to praise Kakoune for having a clean codebase, easy to
navigate and modify. And for good reason! Written in C++, the code uses the
smallest amount of bells and whistles possible to keep the code elegant,
compilable with (reasonably) old compiler versions, but more importantly
convenient.

And when it comes to convenience, Kakoune has some interesting assets your
project could benefit from:

- a header-only implementation of a diffing algorithm
([diff.hh](https://github.com/mawww/kakoune/blob/master/src/diff.hh))
- a regex engine mostly following the ECMA syntax — this implementation
  allowed the project to drop
[boost::regex](https://www.boost.org/doc/libs/1_74_0/libs/regex/doc/html/index.html)
  as a dependency
([regex.hh](https://github.com/mawww/kakoune/blob/master/src/regex.hh))
- a minimal JSON (un)marshaller
([json.hh](https://github.com/mawww/kakoune/blob/master/src/json.hh))
- a custom hash map implementation
([hash_map.hh](https://github.com/mawww/kakoune/blob/master/src/hash_map.hh))
- wrappers for string types (e.g. string view) and associated utilities:
  join, wrap, split, quote, pad etc.
([string.hh](https://github.com/mawww/kakoune/blob/master/src/string.hh)
· [string_utils.hh](https://github.com/mawww/kakoune/blob/master/src/string_utils.hh))
- various functional range filters: filter, transform, gather, map etc.
([ranges.hh](https://github.com/mawww/kakoune/blob/master/src/ranges.hh))
- an implementation of Go's defer statement that runs code once the execution
  flow leaves the current scope
([Go specification](https://golang.org/ref/spec#Defer_statements)
· [utils.hh](https://github.com/mawww/kakoune/blob/master/src/utils.hh#L53))

The above snippets are not exactly drop-in, as they are still coupled to
custom types defined for the editor, but should nonetheless be adaptable
without much difficulty to other C++ projects.

From its user interface
-----------------------

Originally an easter-egg that savvy users found out about by reading the
code that handles the terminal client's user interface, the Clippy character
has become a mascot that is now enabled out of the box. However, although
it's undeniable that nostalgia for Microsoft Office's assistant has fuelled
prolonged interest in Clippy itself, the easter egg's notoriety has cast a
shadow on the larger feature it's a prisoner of: the auto-info pop up window.

The auto-info window is a big contributor to the general level of
interactivity the editor provide, as it pops up any time the user hits a
key in normal mode or has typed a function name in the command prompt. Its
purpose is to provide instant feedback to the user, communicate usage
information or possible options that are available to the user. Every time
I'm using a terminal program that lets me type commands but never hints
at what parameters they take, I sorely wished more people would steal that
from Kakoune!

Another command prompt related improvement that the editor proposes is
fuzzy matching: the user doesn't need to type out letters that make up
the name of the command they need in order, which makes for much faster
completion selection, and increased discoverability.

All command names in Kakoune are WORDS that start with the name of the
functionality group they belong to. The examples below follow:

- to figure out what commands interact with the buffer, typing `:buff`
  would return candidates like `buffer-next`, `lint-buffer`,
  `format-buffer`…
- to call the `lint-buffer` command, typing `:lb<tab>` would insert the
  entire command name in the prompt

Use Kakoune once, and you'll wish your browser enabled fuzzy
matching in your history/bookmarks for the rest of your days. But
you might wonder: there are individual tools that handles
fuzzy-matching, like [fzf](https://github.com/junegunn/fzf),
[ctrlp](https://github.com/kien/ctrlp.vim) or
[fzy](https://github.com/jhawthorn/fzy), what if the user would rather
use them to handle opening, for example, files? Great question! Read on,
that's the next dimension I want you to steal from.

From its philosophy
-------------------

The UNIX philosophy states that tools should focus on doing one thing,
and do it well. The implications are that tools that implement too many
unrelated features end up providing users with an underwhelming experience
because they only allow so much granularity over their behaviour, and that
their maintainers are spread too thin to improve/fix them.

If we re-frame this into the context of text editing, editors should only
worry about exactly that — text editing. And Kakoune does its job as
a UNIX citizen brilliantly, but it also goes one step further: it allows
other tools to interact with it, via shell scripting.

Remember the case of spawning a third-party fuzzy matching program,
above? Without getting into details, in Kakoune you'd implement that by
spawning a new terminal (or pane/tab), which would run the program, and
its output would be interpreted by the editor. Users are free to run any
program they want, any terminal or multiplexer they prefer.

And the concept isn't bound to terminal programs either, although they are
probably the type of tools that Kakoune users would intuitively want to
interact with, on account of the editor being one itself. For example, do
you want to edit a file using a graphical interface? Try the following:

	:edit %sh{zenity --file-selection}

If that doesn't sound anything special, it means that it makes
sense. Unfortunately, the field of text editors on UNIX systems has over
the years turned into an archipelago, in which every editor aims at being an
island. Job management, shell, terminal emulation, window multiplexing…
Text editors have turned into closed ecosystems (or Integrated Development
Environments) that provide many (sometimes cardboard-looking) features
unrelated to editing, which new comers have to buy into, or be left out in
the cold.

So here's an idea everybody should not feel guilty about stealing, if
applicable to their projects: don't re-invent the wheel, we have enough
bad imitations already[^1] — instead, work on ways to make your tools
interface with others more easily!

If you have comments or questions, feel free to drop by the official IRC
channel: #kakoune @ FreeNode.

[^1]: <https://www.oreilly.com/radar/do-one-thing/>
