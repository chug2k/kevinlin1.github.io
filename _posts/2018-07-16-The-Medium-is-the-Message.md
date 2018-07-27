---
layout: post
title: The Medium is the Message
excerpt: >
  Understanding what a computer is, and what it can do.
---

> I read McLuhan's *Understanding Media* and understood that the most important
> thing about any communications medium is that message receipt is really
> message recovery: anyone who wishes to receive a message embedded in a medium
> must first have internalized the medium so it can be "subtracted" out to
> leave the message behind. When he said "the medium is the message" he meant
> that you have to become the medium if you use it. That's pretty scary. It
> means that even though humans are the animals that shape tools, it is in the
> nature of tools and man that learning to use tools reshapes us. So the
> "message" of the printed book is, first, its availability to individuals,
> hence, its potential detachment from extant social processes: second, the
> uniformity, even coldness, of non-iconic type, which detaches readers from
> the vividness of the now and the slavery of commonsense thought to propel
> them into a far more abstract realm in which ideas that don't have easy
> visualizations can be treated. McLuhan's claim that the printing press was
> the dominant force that transformed the hermeneutic Middle Ages into our
> scientific society should not be taken too lightly---especially because the
> main point is that the press didn't do it just by making books more
> available, it did it by changing the thought patterns of those who learned to
> read. Though much of what McLuhan wrote was obscure and arguable, the sum
> total to me was a shock that reverberates even now. The computer is a medium!
> I had always thought of it as a tool, perhaps a vehicle---a much weaker
> conception. What McLuhan was saying is that if the personal computer is a
> truly new medium then the very use of it would actually change the thought
> patterns of an entire civilization. He had certainly been right about the
> effects of the electronic stained-glass window that was television---a
> remedievalizing tribal influence at best. The intensely interactive and
> involving nature of the personal computer seemed an antiparticle that could
> annihilate the passive boredom invoked by television. But it also promised to
> surpass the book to bring about a new kind of renaissance by going beyond
> static representations to dynamic simulation. What kind of a thinker would
> you become if you grew up with an active simulator connected, not just to one
> point of view, but to all the points of view of the ages represented so they
> could be dynamically tried out and compared?
>
> --- Alan Kay, *User Interface: A Personal View* (1989)

One of the things that is most jarring about learning computer science at
Berkeley is just how different it is from the traditional, socially-accepted
definition of 'computational literacy'. There are young people who are 'good'
with technology, and older folks who aren't as 'good' with technology.

Even if you never considered yourself as one of those who are particularly
'good with technology', chances are, if you're at a university in a first-world
country, you've probably used a computer extensively. Through the course of
primary, middle, and high-school, what many considered being 'good with
computers' meant being good at using computers as a tool to compose documents,
make simple edits to photos and videos, type at a reasonably fast speed, and so
forth.

What is so challenging about teaching introductory computer science to students
within this social context is that it depends greatly on the design of the
software. Students form an understanding of what computers can do by means of
the programs they use on the computers. And the programs present only a limited
abstraction over the true power of a computer.

Consider one of David Parnas's classic software engineering papers, *[Use of
the Concept of Transparency in the Design of Hierarchically Structured
Systems][]*. He presents the idea of the *"Transparency" of an Abstraction*
through the loose example of a steering wheel.

[Use of the Concept of Transparency in the Design of Hierarchically Structured Systems]: https://dl.acm.org/citation.cfm?id=360913

In the case of the word processor, it presents a very high-level *virtual
machine* whose operations allow for the composition, modification, and
reformatting of documents, but only through very precise abstractions. It is
equipped with several features which enable the user insert, remove, or replace
text, to make selections, modify the style of text, embed images, and so forth.
These commands can be combined in interesting and potentially infinite ways:
text can be added, removed, or otherwise modified in a document, bolded,
italicized, underlined, right-aligned, made bigger, wrapped around an image,
and so forth.

The word processor defines an interface for how the user can interact with it,
but there are fundamental limits in its design which prevents it from being
stretched in unexpected directions. For example, try editing an image using
only the basic features provided by a word processor. It is a clumsy experience
at best, but it can be done given a deep-enough understanding of the
abstractions provided by the software. Part of the idea of being 'good with
computers' is mastering these abstractions provided by graphical software.

However, the GUI programs that we use on computers differs fundamentally from
the kinds of programs we write in traditional computer science courses like CS
61A, CS 61B, and CS 61C. A graphical program like a word processor is
fundamentally event-driven and *modeless*, ready to respond at the touch of a
button. Multiple word processors can be running on the same computer, supported
seamlessly by the operating system. In comparison, the first programs we write
function much more simply: they execute, processing the input, and then
exiting, returning the output. In some ways, they're not too different from how
event-driven programs are implemented, but there's still a large conceptual
leap moving from interactive graphical programs to more mathematical functions.
How this is experienced can be even more jarring to students as a Python or
Java program is only ever working one line at a time, while graphical programs
seem to be capable of processing a multitude of inputs at the same time.

One of the greatest challenges of the first few weeks of an introductory
computer science course might be overcoming this abstraction barrier posed by
decades of prior experience working with event-driven programs. Some part of it
is about setting expectations for the course and what computer science really
is: not so much about using computers, but about understanding the field of
computational problems and representations for those problems and solutions.

The alternative to all of this could be to embrace the event-driven model:
there's a case to be made about how a browser-based Javascript web-app is a
better introduction to computer science than teaching students the Von Neumann
architecture from the ground-up because it requires less of a conceptual break
from their working understanding of what a computer is and what it an do. The
idea of a computer executing one line at a time is still a somwhat foreign idea
to many students as evidenced by the numerous studies which have shown the
presence of such the *[superbug][]* (like the *Parallelism Bug*), many of which
may arise from these fundamental assumptions about how computers work.

[superbug]: https://web.stanford.edu/~roypea/RoyPDF%20folder/A28_Pea_86.pdf

Alan Kay's argument for *Doing with Images makes Symbols* is one that stands
out to me in its appreciation and understanding of the cognitive science of a
computer user. (Rephrasing of a figure from *User Interface: A Personal View*.)

- **Doing** is like mastering the mouse: it is an *enactive* process where
  mastery of the skill requires knowing "where you are" and how to "manipulate"
the representations shown by the interface.
- **with Images** is like mastering the icons and windows of the operating
  system: it is an *iconic* process which requires recognizing, comparing,
configuring, and a concrete knowledge of the model of the system.
- **makes Sounds** is like mastering Smalltalk: it is a *symbolic* process
  which requires tying "together long chains of reasoning" and relies on
abstract knowledge of the system.

The parallels between the past and the present are striking. Each 'level'
unlocks greater capabilities and greater access to the underlying computer and,
therefore, also requires a deeper understanding of how the computer works in
order to do things with the computer. Designing a course with more of this
context in mind may help with adjusting to the unfamiliarity of computer
science. Explicit treatment of this difference may help students more easily
transition into the rigorous, mathematical, and precise treatment of computer
science we teach in CS 61A, for example. Of course, it won't be as simple as
just directly telling them: these assumptions about what parts the model of the
computer is responsible for versus, say, what parts the operating system is
responsible for, are so deeply ingrained that they appear subconsciously even
if a student would normally deny that the computer is a 'thinking machine' (the
*[superbug][]*).