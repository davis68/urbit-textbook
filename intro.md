The whole textbook will be written as a dual online–printed artifact so I can keep it up-to-date.  Concepts like `%clay` will be explained at the highest level, then step down into particulars so that the implementation details can be changed for future versions of Hoon.

The audience for the text consists of those with prior programming experience who are interested in understanding the Urbit kernel in sufficient depth to develop serious userspace applications atop the platform.  It should provide a window for kernel developers to get their feet wet but won't go as deeply into kernelspace development.

There should be a modest set of exercises per section, on the order of five to ten as with a good advanced math textbook.

The book will be made available online similar to Predrag Cvitanović's [_Group Theory:  Birdtracks, Lie’s, and Exceptional Groups_](http://birdtracks.eu/) textbook, although it also makes some sense professionally to find a publisher like Springer or Wiley or Cambridge.  I envision licensing it under CC-BY-NC if I can arrange an amenable publisher.

There are several possible pathways through this textbook.  Notably, the chapter on Nock may be skipped on a first reading and returned to after other chapters have been completed; references to Nock in the Hoon chapters have largely been posted as asides.

Some of the supporting material, like the Urbit API and Aqua, may be useful to introduce earlier for advanced classes.

1. A Brief Introduction
    1. Urbit Address Space
    2. Accessing Urbit
    3. Developing on Urbit (→ Appendix?)
2. Nock
    1. Primitive rules and the combinator calculus
    2. Compound rules
    3. Kelvin versioning
3. Elements of Hoon (only the 20 necessary runes)
    1. Reading the Runes
    2. Irregular Forms
    3. Hoon as Nock Macro
    4. Key Data Structures
        1. Cores, Doors, Gates
        2. Molds
        3. Maps, sets, trees
    5. Generators
        1. Naked
        2. %say
        3. %ask
    6. Libraries
    7. Unit Tests
4. Advanced Hoon (the rest of the non-obscure runes)
    1. Cores
        1. Metallicity/variadicity
        2. Common Patterns
    2. Molds
        1. Polymorphism
    3. Rune Families
    4. Marks and Structures
    5. Helpful Tools (`++cury`, `++cork`, zap runes, etc.)
    6. Deep Dives
        1. Text Stream Parsing
        2. JSON
        3. Sail/XML
5. The Urbit Kernel
    1. Arvo
        1. `%unix` Events
    2. Zuse + Lull
        1. Hoon Parser
    3. Azimuth
    4. Ames (Major)
    5. Behn (Minor)
    6. Clay (Major)
        1. Ford
        2. Scrying
        3. Marks & conversions
    7. Dill (Minor)
    8. Eyre + Iris (Major)
    9. Gall (Major)
        1. Walkthrough:  Time (Clock)
        2. Walkthrough:  Chat CLI
        3. Walkthrough:  Publish
        4. Walkthrough:  `graph-store`
        5. Walkthrough:  Drum/Helm
        6. Walkthrough:  Bitcoin Interface
        7. Walkthrough:  Bots (Eliza etc.)
    10. Jael (Minor)
    11. Spider (Threading)
6. Supporting Urbit
    1. Booting and Pills
    2. Urbit API
    3. Nock Virtual Machines
        1. ++mock
        2. Vere
        3. Jaque
        4. King Haskell
    4. Aqua & OTAs
    5. Jetting
        1. Jet matching, dashboard, etc.
7. Appendices
    1. Comprehensive Table of Hoon Runes
    2. Hoon versions
    3. Nock versions
    4. Hoon Comparison with Other Languages (Lisp, Haskell, OCaml)
    5. Zuse/Lull versions
    6. Textbook Changelog

---

https://github.com/timlucmiptev/gall-guide/blob/master/workflow.md
https://github.com/timlucmiptev/gall-guide/blob/master/lifecycle.md
https://github.com/timlucmiptev/gall-guide/blob/master/ford.md
https://github.com/famousj/gentle-gall-intro

---

what do yall do for debugging hoon? the only thing i have in my toolbox is ~& and i figure there must be other tools
~master-morzod
5:16 PM
there's also ~| and ~!

poproxoɹdod
5:57 PM
i should have been more specific - i meant ~& as shorthand for "debugging printfs". are there any debugging tools beyond that? i feel like i would have heard of a hoon-specific one by now if there were one, but like can you e.g. use gnu debugger for anything other than like getting stack traces from core dumps (that being literally the only thing ive ever used gdb for - idk how general of a tool it is)

𐐝𐐮𐐾𐐮𐑊𐐰𐑌𐐻𐐨 · Sigilante
6:03 PM
isn't there a profiler?
~master-morzod
6:12 PM
there's two
and you can ctrl-c anytime to get a stack trace
there's no interactive debugger
ctrl-c kills the event, of course. it'd be nice to have a signal that prints a trace and keeps running
-j run a tracing profiler, writes json output to .urb/put/trace/
those files can be visualized in chrome's about:tracing
-P runs a sampling profiler, and prints the output when you exit
the latter is only useful if your binary was built with U3_CPU_DEBUG
CPU_DEBUG=1 ./configure or whatever
