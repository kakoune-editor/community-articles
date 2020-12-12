---
title: Results and their interpretation for the First Kakoune Community Survey
author: Frank Lenormand
author-handle: lenormf
license: CC BY-SA 4.0
---

You'll find below the results to the (now closed)
[First Kakoune Community Survey](https://s.surveyplanet.com/hYB1V90ul),
as well as general [takeaways](#takeaways) derived from them. An interpretation
of the data is also provided when relevant. All the specific questions
(e.g. the multiple-choice ones) that were asked had for objective to shed some
light on a specific point, interpreting the replies is a useful indicator of
whether the contributors to the [Kakoune editor](https://kakoune.org/) are
headed in the right direction, are aware of the biggest problems the users
face, and have an accurate vision of how the tool is being used in the wild.

Note that the raw free-writing type answers will not be attached to this post,
as I cannot extract them easily out of the survey platform used for polling.
I also wouldn't like users to hesitate to be open about their opinions of
the editor in future polls, out of fear that their words might end up being
published (albeit without any identifying information attached to them).

Thanks to the 151 respondents who have donated their precious time to take
the survey!

**Note**: There are only a couple of such questions in the poll, but the
percentages in some doughnut graphs are not accurate! The survey platform
fooled me into thinking the number associated with a frequency would be an
index, to facilitate statistical analysis via programming. Those turned out
to be weights for rating computation (second column named
“Rating” on the pictures). Changing the values after the fact in the
survey platform's interface resulted into the data being corrupted and
unusable, so read the *Adjusted data* when I provided them, they're the
real numbers.

The questions
-------------

### Q1: How did you learn about Kakoune?

[
    ![Question 1]({{site.baseurl}}/assets/img/community_survey_01/question_1-how_did_you_learn_about_kakoune.png)
]({{site.baseurl}}/assets/img/community_survey_01/question_1-how_did_you_learn_about_kakoune.png)

Social information sharing platforms are the crossroad that directs users
towards Kakoune, by far.

Hits from the “internet highway” (search engines) have a low conversion
rate in comparison, which could indicate that some SEO work needs to be
done on the main site.

Despite being as big as personal recommendations and web searches, the
“other” category only presents separate, unrelated, anecdotal data points.

### Q2: Have you ever personally recommended Kakoune to a anybody, in person or online?

[
    ![Question 2]({{site.baseurl}}/assets/img/community_survey_01/question_2-have_you_ever_personally_recommended_kakoune_to_anybody_in_person_or_online.png)
]({{site.baseurl}}/assets/img/community_survey_01/question_2-have_you_ever_personally_recommended_kakoune_to_anybody_in_person_or_online.png)

Two-thirds of users report having personally recommended the editor to
somebody else. It shows that the tool has a significant enough impact on its
users that most of them would get out of their way to recommend it to others.

However, when stacking these replies with those to the previous question,
we can see that a low percentage of those recommendations have resulted in
a user adopting Kakoune.

### Q3: How often do you use the editor?

[
    ![Question 3]({{site.baseurl}}/assets/img/community_survey_01/question_3-how_often_do_you_use_the_editor.png)
]({{site.baseurl}}/assets/img/community_survey_01/question_3-how_often_do_you_use_the_editor.png)

Adjusted data:

- daily: 56%
- rarely: 29%
- weekly: 10%
- monthly: 3%

Being branded as a code editor, it's not surprising that most users report
using Kakoune daily.

Close to one third of users report using it “rarely”, which is an
unexpected outcome. The silver lining could be that those users still find
a corner-case use to the editor on occasion, which apparently cannot be
better fulfilled with any other tools. I'll take 45 “rarely”s over
45 “never”s!

### Q4: How long have you used Kakoune, regardless of frequency of use?

[
    ![Question 4]({{site.baseurl}}/assets/img/community_survey_01/question_4-how_long_have_you_used_kakoune.png)
]({{site.baseurl}}/assets/img/community_survey_01/question_4-how_long_have_you_used_kakoune.png)

Adjusted data:

- less than a year: 60%
- a few years (1-3): 32%
- a long time (more than 3 years): 6%

A reasonable amount of users have stuck around over the years. Future
surveys will tell us more about the tool's retention rate, but I'm confident
considering the increasing frequency of discussions in the community (forums,
IRC, reddit etc.).

### Q5: Do you use Kakoune for work? If yes, what do you mainly use it for?

[
    ![Question 5]({{site.baseurl}}/assets/img/community_survey_01/question_5-do_you_use_kakoune_for_work.png)
]({{site.baseurl}}/assets/img/community_survey_01/question_5-do_you_use_kakoune_for_work.png)

Out of 142 respondents, 3 explicitly stated they do not use the editor for
work (in “other”), and 9 did not reply since the question is predicated
on whether the respondent does use Kakoune for work. 92% of users trust
the editor to help them fulfill their job duties. That's a badge of
honour in itself considering the focus other bigger editors/IDEs (Integrated
Development Environment) place on a self-awarded stamp of work-friendliness,
and the total absence of it in Kakoune.

Another nice surprise is that 5% of respondents who use Kakoune for work
mostly write generic prose with the editor, showing that the editor is a
versatile tool that doesn't only appeal to programmers.

### Q6: What statements best describe how you use Kakoune?

[
    ![Question 6]({{site.baseurl}}/assets/img/community_survey_01/question_6-what_statements_best_describe_how_you_use_kakoune.png)
]({{site.baseurl}}/assets/img/community_survey_01/question_6-what_statements_best_describe_how_you_use_kakoune.png)

The results are in line with the answers to the previous question. The
resolution of the way users interact with the tool is increased here, as
almost 20% of users have selected two or more statements (different than
“other” or reiterated in the “other” form that they use Kakoune as
a specialised tool, option 2). This reveals that the editor is in fact no
just a uni-dimensional tool, but a convenient utility suitable in separate
situations.

### Q7: What is your job title?

As a way to compliment the answers to the previous questions (*how* the tool
is being used), respondents indicated in *what* capacity they interacted
with Kakoune.

Here are the fields the respondents work in:

Software Engineering: 79%
Student: 7%
Science related fields (data science, mathematics, research…): 5%
Unemployed: 2%

Note that one respondent works as a Musician, and another does programming
as a hobby, proving once again the versatility of the tool.

### Q8: What system(s) do you use Kakoune on?

[
    ![Question 8]({{site.baseurl}}/assets/img/community_survey_01/question_8-what_systems_do_you_use_kakoune_on.png)
]({{site.baseurl}}/assets/img/community_survey_01/question_8-what_systems_do_you_use_kakoune_on.png)

- 139 respondents use Linux (the poll shows 138, but one respondent used the
  `other` field to specify `GNU/Linux`)
- of those, 50 use the editor on another system, along with Linux; 35 out
  of those 50 respondents use Mac
- 99 respondents use the editor on only one system: 89 exclusively use Linux, 8 Mac
- out of the 7 respondents who mentioned using Windows, only one uses it
  exclusively, all other respondents declared using it along with Linux

The above data helps figure out which systems should be prioritised in terms
of support: most users only use Linux, and roughly half as many exclusively
use Mac.

However, the numbers also reveal that many use Kakoune on several systems
at once, fortunately the most popular combination is comprised of Linux
and Mac, so the previous data point did not hide anything.

A statistically relevant amount of users (<10% in all), albeit comparatively
small compared to the core of Linux/Mac users, uses BSD, Windows, WSL,
Illumos, NixOS. Future surveys will reveal if these populations are growing,
and if support for those platforms should be watched more carefully (even
though any user reporting an issue on any platform they're using will get
help if possible).

### Q9: Is Kakoune your main code editor? If yes, what other editor were you mainly using before switching over to Kakoune? If not, what is preventing you from switching over to Kakoune?

After reading all the replies and taking count, I found that:

- 75 respondents use Kakoune as their main editor, and stated switching
  over from the following editors (5 have not documented that information):

    - 35 Vim
    - 18 NeoVim
    - 9 Emacs
    - 6 VScode
    - 2 Vis

- 68 respondents do not use Kakoune as their main editor, and 42 among them
  have kindly stated what editor they use instead:

    - 23 Vim
    - 6 NeoVim
    - 5 Emacs
    - 5 VScode
    - 2 Sublime Text
    - 1 RStudio

The most common reasons that held respondents back from switching over were:

- no time or motivation to learn
- difficult to add support for custom languages
- some plugins were not implemented for Kakoune
- too tedious to migrate the user configuration

### Q10: Do you use third-party plugins written by the community?

[
    ![Question 10]({{site.baseurl}}/assets/img/community_survey_01/question_10-do_you_use_third_party_plugins_written_by_the_community.png)
]({{site.baseurl}}/assets/img/community_survey_01/question_10-do_you_use_third_party_plugins_written_by_the_community.png)

Two third of respondents do use plugins written by members of the community,
which hints us that there is an ecosystem that delivers useful extensions
to the editor.

### Q11: Do you write custom Kakoune scripts?

[
    ![Question 11]({{site.baseurl}}/assets/img/community_survey_01/question_11-do_you_write_custom_kakoune_script.png)
]({{site.baseurl}}/assets/img/community_survey_01/question_11-do_you_write_custom_kakoune_script.png)

Most users don't need to write their own plugins, which could mean that
those already available cover the most common needs among the community,
or that they simply don't need to extend the editor with plugins (it already
“just works”).

I could also be that most users don't care to implement the features they're
lacking, and just stick around until somebody else does.

### Q12: Do you publish those scripts online (on Github, Gitlab etc.)?

[
    ![Question 12]({{site.baseurl}}/assets/img/community_survey_01/question_12-do_you_publish_those_scripts_online.png)
]({{site.baseurl}}/assets/img/community_survey_01/question_12-do_you_publish_those_scripts_online.png)

According to the data from question #11, roughly half of respondents
that write plugins publish them online to be used by the community.

This could mean that the average plugin is so small that it's not seen as
worthy of being published.

### Q13: What plugins do not exist yet that you wish were available?

The replies to this question are quite spread out, with most suggestions
being mentioned only by a single respondent. Here are the ones that appeared
six times, making up the most mentioned suggestions:

- support for [tree-sitter](https://github.com/tree-sitter/tree-sitter)
- better support for the [Language Server Protocol](https://microsoft.github.io/language-server-protocol/)
- an advanced Git wrapper, similar to [Magit](https://github.com/magit/magit)
  or [Fugitive](https://github.com/tpope/vim-fugitive)

The following suggestions were all suggested 3 times each, and follow the
above in the list:

- a diff viewer, similar to [VimDiff](http://vimdoc.sourceforge.net/htmldoc/diff.html)
- support for the [OrgMode](https://orgmode.org/) format
- [code folding](https://github.com/mawww/kakoune/issues/453) support
- better support for fuzzy-matching, similar to
  [fzf](https://github.com/junegunn/fzf); one respondent mentioned the ability
  not to have to use a multiplexer to open a file found via the utility

Among the anecdotal suggestions, here's a list of those I find interesting:

- a browsable undo tree
- a scroll bar
- a set of commands to interact with Git hunks (select, revert etc.)
- a wrapper of `:make` that handles more error formats
- a merge tool for Mercurial
- an integrated Python debugger

Note that some suggestions (not given here) were not entirely relevant,
as they were more of a bug report, feature request of generic remark that
were not related to plugins.

This is useful information, as it helps directing the efforts of contributors
who would want to implement a plugin, backed with data.

### Q14: In what language(s) do you read software documentation in, on your system?

[
    ![Question 14]({{site.baseurl}}/assets/img/community_survey_01/question_14-in_what_languages_do_you_read_software_documentation_in_on_your_system.png)
]({{site.baseurl}}/assets/img/community_survey_01/question_14-in_what_languages_do_you_read_software_documentation_in_on_your_system.png)

The editor assumes that most of its users are comfortable reading its
documentation and user interface in English, which is comforted by the
data above.

As this survey is only available in English, we can't know if some users would
benefit from the documentation being translated into their native language
(they probably haven't responded at all if English is a problem to them). The
localisation data above is nonetheless an interesting metric to keep an
eye on, for future surveys.

### Q15: What is your favourite way to get an answer to your questions?

[
    ![Question 15]({{site.baseurl}}/assets/img/community_survey_01/question_15-what_is_your_favourite_way_to_get_an_answer_to_your_questions.png)
]({{site.baseurl}}/assets/img/community_survey_01/question_15-what_is_your_favourite_way_to_get_an_answer_to_your_questions.png)

The objective of this question was to determine whether the documentation
was a good enough resource to provide users with answers, and where it
stood in comparison with other interactive means of getting information.

43% of respondents use the on-board documentation as a primary source of
information when they need to have their questions answered, far ahead of
interactive mediums such as Github, Discuss or IRC, and that's great news! The
documentation is far from perfect and has long ways to go before it can get
anywhere close to that point, but it shows that it's better than “good
enough” considering its popularity.

Multiple respondents who selected “other” mentioned a
[Discord channel](https://discord.gg/q5WwApB) and the project's
[Github wiki](https://github.com/mawww/kakoune/wiki), which I didn't even
consider as possible options — one more blindspot lit up!

### Q16: How would you qualify the learning curve of the editor?

[
    ![Question 16]({{site.baseurl}}/assets/img/community_survey_01/question_16-how_would_you_qualify_the_learning_curve_of_the_editor.png)
]({{site.baseurl}}/assets/img/community_survey_01/question_16-how_would_you_qualify_the_learning_curve_of_the_editor.png)

Adjusted data:

- easy, I got a hang of things with no real difficulty: 70%
- steep, it took me several weeks to be productive: 29%

The results look polarising, because (for some reason) one possible answer
that was supposed to be available to respondents is missing:

- average, I had to read some documentation but got started right afterwards

6 people (1%) did not answer the question, because I reckon neither of the
answers made available to them was aligned with their opinion. There is
also a sizable chance that respondents who would have selected the answer
above instead downgraded/upgraded their answer into either of those available.

A conservative interpretation of this erroneous result is that users *seem*
to be able to switch over to Kakoune reasonably easily, but improvements
still have to be made to the onboarding process considering how many seem
to have had difficulties at the start.

### Q17: Do you run the development (i.e. from the Git repository) or stable (official releases) version?

[
    ![Question 17]({{site.baseurl}}/assets/img/community_survey_01/question_17-do_you_run_the_development_or_stable_version.png)
]({{site.baseurl}}/assets/img/community_survey_01/question_17-do_you_run_the_development_or_stable_version.png)

70% of respondents run a version Kakoune provided by their
distribution/package manager.

This could be an indicator that users install the editor via the simplest
means possible, and are productive enough with the official releases that
they don't need to bother compiling the source code themselves.

On the other hand, almost a third of respondents *do* go out of their way
to keep up with the development version, which could signal that releases
do not happen often enough to make bugfixes and features requested on the
issue tracker available.

### Q18: How often do you run into unexpected bugs (crashes, glitches…)?

[
    ![Question 18]({{site.baseurl}}/assets/img/community_survey_01/question_18-how_often_do_you_run_into_unexpected_bugs.png)
]({{site.baseurl}}/assets/img/community_survey_01/question_18-how_often_do_you_run_into_unexpected_bugs.png)

Adjusted data:

- rarely: 91%
- occasionally: 8%
- frequently: 1%

The editor seems to be fairly stable, with most respondents stating that
they rarely encounter bugs.

Note that the single respondent who answered `frequently` also stated that
they `rarely` (question #3) use the `stable` (question #17) releases of
the editor.

### Q19: What country do you live in?

There are only two clearly big communities among respondents:

- United States of America: 34% (49)
- Germany: 12% (18)

A few clusters make up the core of respondents:

- France: 9
- Canada: 6
- Spain: 5
- Austria: 4
- Brazil: 4
- Finland: 4
- United Kingdom: 4

Honorable mentions:

- Australia: 3
- India: 3
- Netherlands: 3
- Poland: 3
- Ukraine: 3

The trailing 28 respondents live in countries that appear only once in
the dataset.

### Q20: Would you be interested in attending an event about Kakoune? Big or small, (inter)national or local, big talks, lightning talks, workshops…

[
    ![Question 20]({{site.baseurl}}/assets/img/community_survey_01/question_20-would_you_be_interested_in_attending_and_event_about_kakoune.png)
]({{site.baseurl}}/assets/img/community_survey_01/question_20-would_you_be_interested_in_attending_and_event_about_kakoune.png)

43% of respondents stated they'd be willing to take part in an event
about the editor, which indicates that it's on its way to being
popular/versatile enough to spawn an engaged community.

### Q21: What do you like least about Kakoune?

In contrast with question #13, the replies to this one were slightly more
clustered, with a clear top four least liked aspects of Kakoune:

- the documentation could be organised better, more comprehensive (10
  mentions)
- reliance on shell for interfacing with third party tools (10 mentions)
- difficulties getting started, lack of tutorials and videos (9 mentions)
- the Kakoune language is hard to read (8 mentions)

Note that respondents sometimes made remarks that counted towards several
items.

The following complaints all sit at five mentions each:

- not enough plugins, immature ecosystem
- no built-in clipboard integration
- the variety of quoting styles in regular scripts can get messy/confusing

The rest of the replies sit at four or less mentions, with most being
mentioned by a single respondent.

Here's a selection of the ones I found interesting:

- scrolling and moving around display-lines is broken
- don't like Clippy
- the online documentation should be rendered in HTML, accessible when
  internet access is available

### Q22: What do you like most about Kakoune?

Although there are different ways respondents to this survey are unhappy
about Kakoune, as we've seen in the diversity of replies made to question
\#21, there seems to be much fewer ways they are happy about it!

By far, respondents enjoy the editing model: it's intuitive, consistent,
predictable, orthogonal, and a refreshing take on the well-known Vim grammar
(49 mentions).

Good, first-class citizen support for multiple selections is also referred
to consistently (32 mentions).

The second cluster of replies praises the editor for being a good
UNIX citizen, allowing interactions with third party tools via shell,
and indirectly any scripting language (23 mentions). This population of
respondents seems to be cohabitating in the community with those who stated
that relying on shell was their biggest grief (c.f. question #21). That
might hint at a fragmented community, polarised between two camps who have
their own views about how far a code editor should take the UNIX philosophy,
but I interpret this result as a positive point: Kakoune's strongest asset
(see above) is so cherished that it's unifying the two sides and retaining
their users.

Instant, visual feedback (often referred to by the respondents as “permanent
visual block mode”) is just as appealing (22 mentions).

The smallest cluster of replies trailing in the statistics revolves around
a minimalist design (15 mentions), fast startup time and low runtime latency
(11 mentions), and ease of use/customisation (11 mentions). This last point
once again comes in contradiction with the replies to the previous question,
in which almost as many mentions (8) were made to how the Kakoune language
was hard to read/use. Some users lean one way, some the opposite way, showing
that there probably isn't a standard “Kakoune user” persona, but instead
a variety of profiles who unite behind the editor's strongest points.

Here are some interesting replies:

- Clippy (8 mentions)
- built-in fuzzy matching (5 mentions)
- good command discoverability (4 mentions)

### Q23: What is something lacking about Kakoune?

Due to how the question is worded and its open nature, many replies given
here were redundant with those to question #13, or should have been mentioned
there. Nonetheless, since the latter was focused on plugins, this one allowed
scanning a wider panel of opinions, which is valuable to avoid blindspots
and detect opportunities.

The most mentioned suggestions roughly combine what respondent dislike most
about Kakoune and what plugins they wished existed, but as with these two
questions, opinions are spread out:

- more tutorials, in video form or interactive/gamified (like VimTutor) (10 mentions)
- a broader community with a more mature plugin ecosystem (10 mentions)
- better organised and more comprehensive documentation (9 mentions)
- code folding support (8 mentions)
- a Graphical User Interface (6 mentions)

Some respondents also had interesting suggestions that didn't come up in
other replies:

- Right To Left text support
- codebase documentation (comments etc.)
- two-way communications with `kak -p`

Takeaways
---------

The replies made by respondents to this survey have been generally
predictable, no major surprises have popped out of the data. This is
comforting because it shows that the original assumptions made about usage
and segment were correct, and that the contributors' vision is aligned with
how users actually benefit most from the tool.

In terms of persona, Kakoune users in majority are Linux adepts, familiar
with the Vim modal edition flavour, who write code, edit configuration files,
and augment the toolset provided out of the box with plugins.

They enjoy the refreshing take on modal editing, first-class support for
multiple selections and the level of interactivity with third party tools
via shell (aka UNIX philosophy).

Documentation and plugins are the biggest issues, which could be due to the
thermal shock induced by switching over from a decades old editor like Vim
to Kakoune. Those are valid concerns nonetheless, which will hopefully
become less and less persistent as contributions are made, and the editor's
ecosystem grows.

Features that are most in demand have not reached consensus, but have been
mentioned enough times to be considered seriously: Language Server Protocol
and Git support, code folding, tree-sitter integration. Other suggestions
have been made, and are communicated regularly, but these seem to have
taken roots now.

Thanks for reading! Feel free to join
[#kakoune](https://webchat.freenode.net/?channels=kakoune) @
**irc.freenode.net** to discuss the survey, ask questions, or idle.
