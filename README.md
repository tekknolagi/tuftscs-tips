# What is this repo?

This repository is a resource for Tufts Computer Science students who are
interested in learning more about the classes they are currently taking.

# What classes are there?

* [COMP 105](#comp-105)
* [COMP 40](#comp-40)
* [COMP 15](#comp-15)

# How can I add my two cents?

Submit a Pull Request. Classes should have the following sections, in order:

1. Topics covered
  * Brief overview (bulleted list) of what gets taught in the class.
2. Tips
  * What would you tell a student coming into the class?
3. Combining material
  * What can the student do during the class to help learn more deeply about
    the material at hand?
4. Other related material
  * What should the student look at next after the course is over? (Or during
    the course, if desired)
5. Tufts resources
  * Who or what at Tufts can be a guiding force or helping hand?

# Classes

## COMP 105

### Topics covered

* Big-Step Operational semantics
* Scheme
* Higher-order functions
* Anonymous functions
* Continuation passing
  * SAT solver
* (S)ML
* Type systems
* Type checking
* Type inference
* Smalltalk and object-oriented programming
* ML modules and functors
* Lambda calculus

### Tips

* Read the book
* Don't just rely on SML/NJ. It tends to have poor error messages. Also try
  MosML and MLton (especially for error messages)
* Don't let the Greek letters intimidate you. They will make much more sense
  after the first lecture.
* Try to read the book's chapters before their corresponding assignments (maybe
  not the whole chapter, but the first 20-30 pages will give you a great
  start). Then it is easier to use as a reference when you are stuck.
* Scheme syntax is mostly new, but easy. It's all stuff you know but in a weird
  order and with a couple extra parentheses. Once you get this you'll be fine.
* As any other class, Halligan Helper gets full the last 2 days of the
  assignment. Be smart and get help before the rest of the crowd.
* Be able to justify each test. What corner cases does it test?
* Most hard homeworks have similar problems in the book, except that these are
  solved for you. Use them for inspiration 😉
* More technical stuff that is good to know (and you'll understand when you get
  to the topic):
  * `append` takes linear (O(n)) time and it's VERY different from `cons` (make
    sure to get the difference right from the beginning).
  * Functions passed to `foldr` and `foldl` have the element as the first
    parameter, and the accumulator as the second.
  * The order in which you pattern match *does* matter.

### Combining material

* Build your own Scheme interpreter while you are learning about uScheme. It
  will help you understand all of the following topics:
  * Operational semantics. You will make mistakes with the semantics of your
    interpreter. Many of them will stem from making incorrect or inconsistent
    assumptions about what should happen when. These ideas are formalized in
    operational semantics.
  * Scheme. Hopefully, since you're interpreting it, you understand more
    deeply how the language functions.
  * Higher-order functions. You'll need these for the standard library of your
    new language.
* Build a language from essentials. It is possible to start from the very
  basics and build a fully-functioning language from that.
  * Lambda calculus. This is a simple but fully Turing-complete language of
    expressions that can be used to bootstrap a fully-featured programming
    language.
  * Proofs of Turing completeness. This has great tie-ins with COMP 170. If you
    can prove that you can transform any program into this language, then you
    have a Turing-complete programming language. Roughly.
* SML, since it has not changed since 1997, has spawned a family of languages
  used by people who like the ideas presented but want to add more practical
  features.
  * [OCaml](http://www.ocaml.org/) and [Haskell](https://www.haskell.org/)
    belong to this family. As Norman once said, "OCaml is for people who like
    SML but would rather be writing C", and Haskell is like SML with a
    ridiculously advanced type system, among other features.
    * [OCaml vs SML](http://adam.chlipala.net/mlcomp/)
    * [F#](http://fsharp.org/) is similar
  * Lazy evaluation. Haskell presents a concept called "lazy evaluation",
    meaning expressions are not (necessarily) evaluated when they are expressed,
    but instead when the results are needed.
* Type systems
  * Hindley-Milner
    * [Wikipedia](https://en.wikipedia.org/wiki/Hindley%E2%80%93Milner_type_system)
    * [So you still don't understand Hindley-Milner?](http://akgupta.ca/blog/2013/05/14/so-you-still-dont-understand-hindley-milner/)
  * System F
    * [Wikipedia](https://en.wikipedia.org/wiki/System_F)
    * [System F vs Hindley-Milner](http://stackoverflow.com/questions/23995736/example-of-type-in-system-f-that-is-not-available-in-hindley-milner-type-inferen)
    * [Story of](http://huoc.org/system-f.html)
  * Linters/static analysis on top of other languages
    * [Wikipedia](https://en.wikipedia.org/wiki/Static_program_analysis)
    * [Static analyis for Python](http://stackoverflow.com/questions/35470/are-there-static-analysis-tools-for-python)
  * Union types
    * [In Crystal](https://crystal-lang.org/docs/syntax_and_semantics/union_types.html)
    * [Blog post](https://yinwang0.wordpress.com/2011/08/28/sum/)
  * Gradual typing
    * [Wikipedia](https://en.wikipedia.org/wiki/Gradual_typing)
    * [Blog post](http://wphomes.soic.indiana.edu/jsiek/what-is-gradual-typing/)
  * Borrow checking, lifetimes, and Rust
    * [Rust](https://www.rust-lang.org/en-US/)
    * [Ownership in Rust](https://doc.rust-lang.org/book/ownership.html)
    * [Borrow checking vs refcounting](https://www.reddit.com/r/rust/comments/30yn1n/what_is_the_difference_between_the_borrow_checker/)
  * Nim lang
    * [Nim](http://nim-lang.org/)
* Smalltalk
  * [Double dispatch](https://en.wikipedia.org/wiki/Double_dispatch)
  * [Ruby](https://www.ruby-lang.org/en/) is a language influenced by Smalltalk and Lisp.
    * [Ruby is an acceptable Lisp](http://www.randomhacks.net/2005/12/03/why-ruby-is-an-acceptable-lisp/)
* Callbacks in other languages, like JS

### Other related material

* Garbage collection
  * [Wikipedia](https://en.wikipedia.org/wiki/Garbage_collection_(computer_science))
* Compilers
  * [Appel's C/Java/ML compiler books](http://www.cs.princeton.edu/~appel/modern/).
    Appel wrote 3 books about writing a compiler for The Tiger programming
    language. He found that students who used ML had an easier time finishing,
    and students who used C did not finish.
    * [Why ML/OCaml are good for writing compilers](http://flint.cs.yale.edu/cs421/case-for-ml.html)
  * Optimization
    * [Wikipedia](https://en.wikipedia.org/wiki/Optimizing_compiler)
  * Language/AST transformations
    * [Reason](https://facebook.github.io/reason/) is a project that provides a
      new front-end for the OCaml programming language. Reason compiles to an
      OCaml AST.
* 170 tie-in
  * Type inference: function parameters cannot have polymorphic types and
    neither can type variables be instantiated with them -- why undecidable?
  * [SAT](https://en.wikipedia.org/wiki/Boolean_satisfiability_problem) solver: reductions, NP-completeness
  * [Regular expressions](https://en.wikipedia.org/wiki/Regular_expression), [regular languages](https://en.wikipedia.org/wiki/Regular_language)
* Lexing and parsing
  * LR/LALR/LR(k)
  * Parser generators
* Anonymous functions in C++
  * [Pick-and-choose closure captures](http://en.cppreference.com/w/cpp/language/lambda)
* Concurrency
  * [Erlang](https://en.wikipedia.org/wiki/Erlang_(programming_language))
* Monads
  * God help you
* Those funky operators like `<*>` and what they mean
* Building an interpreter
  * [Crafting Interpreters](http://www.craftinginterpreters.com/)
  * [Writing an Interpreter in Go](https://interpreterbook.com/)
  * [Scheme from Scratch (C)](http://peter.michaux.ca/articles/scheme-from-scratch-introduction)
  * [Building LISP (C)](http://www.lwh.jp/lisp/)

### Tufts resources

* Fun in the afternoon
  * Functional programming discussion group. Advised by Norman Ramsey.
* The grad TAs
* Norman Ramsey
* Kathleen Fisher

## COMP 40

### Topics covered

* Introduction to C (for those coming from a C++ background)
* The benefits and drawbacks of the pair programming approach
* Using abstraction/modularity to write maintainable code
* Enforcing and reasoning about invariants to ensure program correctness
* Von Neumann architecture (especially: the significance of data and code living in the same memory)
* Reading and writing technical documentation
* Bits, bytes, and nibbles ("bits is bits", i.e.: data is subject to your interpretation)
* More of an in-depth view into what happens during compilation
* Caching and performance measuring
* Low-level arithmetic and representation of numbers
* Bitwise operations
* Reading and writing assembly code

### Tips

* Start the homework early, start the homework early, start the homework early-
  Comp 40 is not a *conceptually* difficult class- its main challenge is in the
  amount of time that you will have to spend coding.  If you start early, you
  will give yourself the time you need to 1. write the bugs that are inevitable
  and 2. fix the bugs and *learn* why they happened, rather than spend the whole
  semester in a debugging panic that teaches you nothing.
* Be an effective pair programmer.  The partners that you find yourself with
  during the semester will, mostly, be people you have never met.  The odds are
  that either they understand the course material significantly better than you,
  or that you understand the course material significantly better than they do;
  very rarely will you and your partner be a perfect match in terms of your
  understanding.  If this happens and they are the ones who understand more, take
  the time to ask them questions about what is going on in the code that you two
  are writing; it is *not* a waste of time, and it will help *both* of you to
  better understand the material.  If you are the one who understands more, be
  sure to stop periodically and check in with your partner.  Being able to
  explain the code and the course topics will reinforce your understanding, and
  might even be fun.
* Become acquainted with sites that contain documentation and Q&A resources,
  such as Stack Overflow and [Tutorials
  Point](https://www.tutorialspoint.com/cprogramming/).  They often have very
  clear examples and explanations of some of the standard library tools you will
  use.  For example,
  [this](https://www.tutorialspoint.com/c_standard_library/c_function_sscanf.htm)
  may be a good place to read about one of the standard library functions you
  will use in the first lab.
* Be an effective HalliganHelper queue resident.  You will spend a lot of time
  on the HalliganHelper queue.  Before speaking with a TA, there are a number
  of steps you should follow:
  * First, you should run your code through a debugger (gdb) and/or valgrind.
    If you don't know how to use one or both of these tools, it is *absolutely*
    worth your time to meet with a TA at the beginning of the semester to get an
    introduction to these tools.  Humans are bad at reasoning about code, so you
    need to have some idea of what is actually going on in your code.
  * you should search google/stack overflow to the best of your ability
  * you should draw pictures, which will help to clarify both pointer questions
    and questions about your design (in terms of interactiosn between modules)
  * you should come up with an educated guess for what you believe the answer
    is, or might be, and why that is the case
  * you should explain to the TA what you have tried already. "My code is
    broken" and "Why is this segfault happening?" are common statements that a
    TA hears when they first walk up to a group, but are not helpful places to
    begin.
* You will be forced to read technical documentation and header (`.h`) files
  that will be provided to you.  If you run into code or jargon that you don't
  understand (especially `typedef` related constructs), you should follow the
  steps above and then talk to a TA if still confused.  Plowing through the
  confusion is rarely the right thing to do, and will cost you, in some cases, a
  significant amount of time.
* Learn effective Googling strategies.  For example, googling
  `site:stackoverflow.com sscanf` will limit your search results to Stack
  Overflow.
* As long as you try your best during the class, the points will work
  themselves out in the end. That's why the staff gives vague grades like "Very
  good", "good", etc.  Don't worry too much about your grades, don't stay in
  Halligan into the early morning hours, and please stay healthy :)

### Combining Material

* Write test programs.  If you are curious "what would happen if..." or "why is
  my code doing xyz...", you should change the code, recompile it, and see what
  changes.
* Look for interesting questions on Stack Overflow's "Related" and "Hot Network
  Questions" sidebars.  There are a lot of interesting pieces of C trivia to be
  found by following those links.
* Write your own assembler for UMASM (the assembly language you write in during
  the last assignment)
* An excellent question asked by a student in COMP 15 one semester:
  * "We learned in lecture that we use a 'class' to store and model state and
    behavior.  I understand how we store state, because that's just data that
    we can store in memory.  But how does a class store behavior?"
  * Spend some time thinking about the answer to this question.  The answer
    reveals a lot of deeper, subtle points about the relationship between code
    and data.
* Explore other low-level, systems level languages such as Rust.  A good
  exercise is to implement the Universal Machine in Rust.
* Since the C standard library is so small, implement various data structures
  or other tools that would be useful to have in a language:
  * Implement various collections (hash tables, sets, etc.)
  * Implement [arbitrary-precision arithmetic](https://en.wikipedia.org/wiki/Arbitrary-precision_arithmetic)
  * Implement a library for precise real number arithmetic (i.e. make it so
    that 0.1 + 0.2 == 0.3)
* Explore compilation (look for links in the [COMP 105](#comp-105) section).
* Design and implement your own VM
* Optimize your existing solutions, and learn about what kind of low-level
  optimizations can be made (bit twiddling hacks, inspecting assembly output,
  etc.)

### Other related material
Comp 40 gives you the tools to explore a large number of other topics:

* [Hardware emulation](https://en.wikipedia.org/wiki/Hardware_emulation)
* Learn about
  [concurrency](https://en.wikipedia.org/wiki/Concurrency_(computer_science))
  and how it works at a low-level
* Go more in-depth with low-level code
  * Read the coolest [stack overflow
    question](http://stackoverflow.com/questions/11227809/why-is-it-faster-to-process-a-sorted-array-than-an-unsorted-array)
    ever
  * Low-level security
    * [Buffer overflow attacks](http://heartbleed.com/) (and also read this
      cool buffer overflow
      [story](http://www.gamasutra.com/view/feature/194772/))
    * [Return oriented programming](https://en.wikipedia.org/wiki/Return-oriented_programming)
    * [This](https://trailofbits.github.io/ctf/exploits/references/tr-2007-153.pdf)
      looks to potentially be a good resource for other low-level security
      exploits.
  * Learn about how potentially life-threatening
    [bugs](https://around.com/ariane.html) manifest themselves in low-level
    code
* Go on to explore higher-level languages, like Python, Java, functional
  languages, etc., using your low-level knowlede to reason about the
  performance of constructs in these languages.
* Find and contribute to open-source projects! This course gives you the ability to read large amounts of code, familiarize yourself with an existing codebase, and write real code.  Put it to use by giving back to the larger CS community!

### Tufts resources
* There are a lot of very smart undergrad TAs. Talk to them and learn from them.
* Mark Sheldon gets very excited about some of the topics in Comp 40. Stop by his office to chat with him!
* Norman Ramsey designed the class
* Noah Mendelsohn is the [chairman of the internet](http://www.arcanedomain.com/computerwork.html) and is in general incredibly smart; he teaches COMP 40 on alternating semesters with Prof. Sheldon. Talk to him too!

## COMP 15

### Topics Covered:
* Your first guide to getting a software engineering job (interview questions!)
* Knowing the difference between the client side and the implementation side 
* Introduction to C++ programs that utilize complex data structures
* Utilizing Object Oriented Programming (OOP) concepts to write better code
* Using abstraction/modularity to break down complex problems
* Allocating and managing dynamic memory and visualizing what happens under the hood (aliasing, deep vs shallow copies)
* Evaluating different data structures (sequences vs linked list, stacks vs queues) 
* Manipulating data structures to make it better (trees, heaps and more!)
* Writing code that must handle MANY test cases and handling exceptions
* Understanding Big O (asymptotic analysis) and why certain choices are better (first step towards becoming an ‘engineer’)
* Reading long documentations (~8 pages PDF) for homework assignments
* Writing technical comments and documents (README) that make your code easier to follow
* RECURSION, recursion, ………, Mark loves RECURSION, hence, so should you
* Debugging is life and you will become master seg fault solver by learning how to use valgrind
* Visualizing sorting (literally, you will become a number to be sorted in class)
* Learning to optimize your code and seeing how your choices of code MATTER!

### Tips:
* Start the homework early and read the homework document early. Comp 15 is a new challenge for comp 11 students and the leap might feel like a lot (this is coming from a comp 11 TA). At times, the document may seem confusing and there may seem like there’s too many things to consider at once. I know that there were students who started homework a few days before and got them done in comp 11. In comp 15, that is NO LONGER an option. You will get STUCK in automatic testing even if your code works with simple input testing. Moreover, if you are confused, so are other students in your class and 2~3 TAs can’t get to over 20 students at once. Really try to start early so that you can discuss your idea with the TA in peace. You will realize that you think a lot clearer when there is no pressure, so really try to start early.
* Before coding, try to draw out what you would like to do. After drawing out your idea, go talk to a TA to see if your code makes logical sense. Even complex ideas like recursion will all make sense once you begin drawing them out. Spend Friday understanding the documentation from the homework assignment, spend Saturday drawing out your idea, spend Sunday talking with your TA about the sketch that you have and then code! The TAs prefer to talk about your sketch and idea than debug with you because debugging code is not only tiring, it takes a lot longer for you to finish your homework or project. Save the misery on both parts by trying out this strategy! If you have a good design, then you will avoid the mess of getting into bugs that are difficult to find. Moreover, if you have a good design, then the TA will likely not have to look at your code and fix your bug by noticing an error in your design. Trust me on this, you will save a SIGNIFICANT amount of time! 
* Become acquainted with data structures. Learn how they work and draw them out with the TAs. Seek the TAs to learn how the complex data structures work instead of seeking them solely for debugging! The TAs for comp15 are an awesome group and all have a very deep understanding of how the data structures work. You will see that even one wrong detail in data structures will lead to segmentation fault quicksand or unexpected behavior. Each code you write really matter, so even if you understand, go check with the TAs to make sure you are crystal clear!
* Decisions, decisions, decisions! There are multiple right answers in data structures, which is why, “am I doing it right?” will give you a very mixed answer in this class. Taking ownership of your decision after evaluating different options is a hallmark of a good engineer, so make sure you have a deep understanding of each data structure you cover in class. There is nothing minor that you can skip in this class, as each new data structure is now a new option you can consider for your upcoming homework or project. Each data structure has its own pros and cons, so learn how to evaluate and choose what you believe is the best for the problem you are trying to solve! 
* Make sure you go to class. Mark does not use a powerpoint, so if you miss one, then you will not have any resources to catch up with class work. So if something happens, make sure you get note from someone and try to never fall behind because the class goes by quick!
* There is no more HalliganHelper, but Piazza is always on to communicate with the TAs. Identify the location of the TAs through Piazza to get help! Also, Mark holds regular office hours and he is of great help if you want a deep understanding of the concepts discussed in class. From my personal experience, he normally takes around 20~30 minutes to explain concepts each time I visited, so if you are in line, you may have to wait quite a time. But once it is your turn, you will get the thorough help that you may need. Mark is awesome during office hours, so do try to take advantage of it!
* Comp 15 debugging tutorial 101:
  * First, you should run your code through a debugger (gdb) and/or valgrind. If you don't know how to use one or both of these tools, it is absolutely worth your time to meet with a TA at the beginning of the semester to get an introduction to these tools. Memory management is new to all comp 11 students and it is essential you learn how to use these tools. You won’t survive without it, so learn it ASAP!
  * Humans are bad at reasoning about code, so you need to have some idea of what is actually going on in your code. Hence, when you see errors, you should draw pictures and bring them to the TAs to clarify both what you intended and what is actually going on in your code. This will help you make a better educated guess and give the TAs a lot more pleasant experience.
  * You should explain to the TA what you have tried already. "My code is broken" and "Why is this segfault happening?" are common statements that a TA hears when they first walk up to a group, but are not helpful places to begin.
* Exams and projects are difficult, but Mark is very understanding. Don’t freak out and know it’s okay to have a low score on the exam because Mark will curve well. He understands that he is throwing a lot at you and will reward you for all your hard work. You may very well be surprised with your final score. For projects in particular, he will likely extend the deadline if the difficulty is too high, so keep working hard and please stay healthy :)

### Combining Material
* Write test programs. We call this unit testing where you make test files for each function that you make. The goal of testing is to try to break your file and be as nasty as you can to it, as you want to prove that your code is very robust against potential hackers! Sometimes, you will be asked to submit your testing file because it is that important! After making the test file, input various arguments into your function that you are testing, even those that are not supposed to work. Make sure that your exceptions work the way you intended. If you are curious "what would happen if..." or "why is my code doing xyz...", you should change the code, recompile it, and see what changes. The most common errors to check are off by 1 errors, exceeding capacity and empty container errors.
* Utilize the object oriented programming concept and learn how to use pointers! Your code will become a lot better once you utilize these concepts and writing functions that are within 30 lines will become a lot easier! If the big ideas that Mark talks about during class is not clear, go to the office hours and get those covered ASAP! The way your code is graded will no longer be solely based on whether your code works. Your design matters too, so really take the initiative to understand the big topics thoroughly!
* If the ideas regarding data structures did not make any sense and you would like more resources, check out mycodeschool on youtube or geeksforgeeks. These are few of the many data structure resources out there that you may use to visualize the concepts. Don’t try to copy off the code as that will ruin your learning experience, but know that there’s a lot out there since data structures is ESSENTIAL for job interviews at top tech jobs. What’s truly important is that you understand how the code works under the hood so that you can show what you know during your future interviews :)
* An excellent question asked by a student in COMP 15 one semester:
  * "We learned in lecture that we use a 'class' to store and model state and
    behavior.  I understand how we store state, because that's just data that
    we can store in memory.  But how does a class store behavior?"
  * Spend some time thinking about the answer to this question.  The answer
    reveals a lot of deeper, subtle points about the relationship between code
    and data.
* Explore different concepts and know why certain errors occur by drawing. Once you draw it out, you will realize that the computers never lie.
*  There are standard template libraries in your book and on-line. Don’t fall into the temptation of using them (unless explicitly told); the purpose of this class is to understand how they work under the hood. If you resort to using other resources, use them for visualization only and for any other help, go to the TAs.

### Other related material
Comp 15 gives you the opportunity to explore what happens under the hood and solve complex problems!
* Learn about valgrind and memory management
* Get the skills to solve complex problems! HackerRank and other interview problems will be solvable after taking this class.
* Learn about how to write code that will be easy to read for others and prevent nasty people who wants to prove your code as ‘breakable’ wrong
* Find out how pointers can break your code and optimize your code. Instead of being clueless, now you will be able to look at code and see why they break! Not only could you break other’s code (but please don’t), you can make someone else’s day by making it work!

### Tufts resources
* There are a lot of very smart undergrad TAs. Talk to them and learn from them.
* Utilize the piazza and ask questions during the labs. Labs are one time where you can ask any question that you discussed in class to people who are super approachable :)
* Mark Sheldon gets very excited about some of the topics in Comp 15. Stop by his office to chat with him!

