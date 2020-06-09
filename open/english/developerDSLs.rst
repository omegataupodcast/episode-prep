I have recently been asked why I always promote DSLs for domain experts
and non-programmers, and not so much for developers. So in this post,
I'll explain my position.

We should probably define what we mean by developer. To me, a developer
is somebody whose main skill is software engineering. They understand
patterns, know relevant technologies and languages, are up to speed with
modern libraries and frameworks and understand and care about
non-functional concerns. Importantly, they can deal with complexity, for
example, by defining their own custom abstractions with the help of
general-purpose programming languages. A significant subset of
developers define themselves specifically with this latter point.

Of course, there are people who use general purpose languages to
implement functional requirements in a particular domain. For example,
in one of my current projects, the people who we built the DSL for
currently use a general-purpose language to implement tax calculations.
I see them really as domain-experts who -- by necessity, lacking a
better alternative -- use the tools of developers. I do not really see
them as developers in the sense of the above definition. And many of
them don't see themselves as developers either.

We must also define the notion of DSL in this context. You can argue
that developers use lots of DSLs, languages that are (perhaps) not
Turing complete and fill a particular niche in the developer's toolbox:
HTML, CSS, SQL, Matlab, make, maven and gradle are some of the examples
that come to (my) mind. However, while these are definitely DSLs, in the
context of this discussion, they are out of scope. The reason is that
these languages are not developed by the organization or team. They are
just there, and most developers don't even consciously recognize them
DSLs. Oh, and I don't consider fluent-API-style internal "DSLs" as DSLs.

So, getting back to the original question at the top: I am indeed
skeptical regarding the development and use of custom domain-specific
languages, developed by their own organization, for people who consider
themselves skilled and competent software developers (and are not really
those "programming domain experts"). Let's explore examples and reasons.

The most important one, in my opinion, is that the benefit just isn't as
great. If you convince your domain experts to use a DSL to formally
specify functionality (instead of writing requirements documents), you
extend programming-style activities to much earlier in the overall
development process (often called front-loading). This can hugely
increase productivity and quality. Replacing a library or framework used by
software engineers by a language that has better syntax and potentially
better static checking just does not have that same leverage.

The second reason hides in the previous paragraph: of course developers
use lots of reusable abstractions in the form of frameworks and
libraries. They might not have as convenient syntax as a good DSL and
are worse regarding analysis and error reporting, but developers are
able (and willing) to deal with this. Domain experts might not be. More
technical reasons: for developers, integration with existing libraries,
frameworks and developer tools is mission-critical. Doing all of this for
a DSL can be a lot of work. Domain experts usually do not rely on such a
wide array of technology, and they prefer to work in a more self-contained
environment that is the DSL and its IDE. 

Another reason is cultural. A DSL by definition restricts the user in
some way (even though it also provides lots of convenient shortcuts for
important behaviors). But developers usually do not want to be
restricted, they want to be able to "express everything" if necessary.
And while incremental language extension in the style of mbeddr or
KernelF-based DSL allow users to "express everything" by reverting back
to the base language, it is still not quite as seamless as with
frameworks and libraries. There are more cultural obstacles. Developers
often don't like to rely on tools they consider off the mainstream,
which language workbenches typically are. And many developers
continuously try to optimize their CV, and to make themselves attractive
to potential future employers. It's important to have stuff on your CV
that is recognized, proprietary DSL of course are not. Note that these
statements here are not judgements -- but they limit the interest in
DSLs.

Of course, many developers build there own utilities to make their task
easier, some of them with quite sophisticated specification syntax that
should be considered DSLs. But usually these systems address only a part
of the development workflow (interface definition, state machines, and 
the temporal specification in the example below), and integration with the
rest of the system happens on the level of the generated code -- developers
don't mind looking at that, in contrast to domain experts.

Let's look at some examples and see what we can learn. The first one is
near and dear to my heart: mbeddr. This is set of incremental extensions
to the C programming language to simplify embedded programming. While we
learned a lot building it and develop lots of skills and utilities on
the way, and better itself is a failure: we were not able to achieve
meaningful use with embedded software developers. We might have all
kinds of mistakes in marketing and sales, but we very definitely ran
into a cultural barrier as well. Many embedded programmers really want
to know every bit personally. This collides with the notion of
abstraction and code generation.

Another failed example. One of the earliest uses of MPS was within
Jetbrains. They had developed a kind of statically typed JavaScript and
DSLs for web UI development. After a while, and after developing actual
products, they abandoned this approach. The reason was that the
developers preferred to use the native web libraries directly. We can
only speculate about the reasons, probably several of those I've
mentioned above played a role. One particular point I heard about is
that the MPS-based approach relied regeneration, whereas the native one
just required pressing Cmd-R in the browser to reload the page.
Apparently the benefit from the DSL did not outweigh this (really not
that huge) slowdown.

Another one, this time not a failure. At my current customer, developers
have to deal with bi-temporal logic. They have developed a little
specification language to specify the temporality of the data that could
then be used within a function. While there is simple specification
language, this tool really falls more into the category of utility and
it's not a full-blown DSL. This one was used in production, by technical developers.

As soon as the developer's task becomes more than writing code and
tests, the picture changes a little bit. For example, at OHB, the C code
they write has to conform to architectural standards governed by ESA,
and the developers have to document their conformance. At least some of
the developers there are willing to use (and build) their own DSL to
automatically generate all the stuff required from them beyond code. I
can report a similar example from the healthcare domain, where we built
a DSL that would eventually be used by healthcare domain experts. But
initially it was also used by developers, sometimes pair-programming
with the doctors, and apparently they liked it as well. Again,
healthcare regulations require lots of derived metrics and
documentation, and the benefits of a DSL become more obvious. There are
also examples for DSLs in the automotive domain, for describing
interfaces, state machines and contracts. But as I have said above,
these languages and their generators play only a relatively small role
in the overall development activities of the engineers.

There's another example of successful use of DSLs for developers: for
language definition! Many language workbenches are effectively collections
of DSLs for language definition, and the language engineers happily use
them (even though there is also Rascal which relies more on libraries).
But they are kinda biased regarding DSLs and might not suffer from these
cultural issues I mentioned above.

So where does that leave us? Building your own DSL is a harder sell when
you target users whose primary skill is software engineering, for
technical and cultural reasons. In addition, there's usually not as much
leverage compared to building one for domain experts. That's why I emphasize
DSLs for non-programmers.

Acknowledgements: I want to thank Tamas Szabo, Sergej Koszejev and Klaus Birken
for feedback on the text that helped me sharpen my thoughts and improve the text.
