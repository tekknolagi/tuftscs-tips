# What is this repo?

This repository is a resource for Tufts Computer Science students who are
interested in learning more about the classes they are currently taking.

# What classes are there?

* [COMP 105](#comp-105)
* [COMP 40](#comp-40)

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

* Start the homework early, start the homework early, start the homework early- Comp 40 is not a *conceptually* difficult class- its main challenge is in the amount of time that you will have to spend coding.  If you start early, you will give yourself the time you need to 1. write the bugs that are inevitable and 2. fix the bugs and *learn* why they happened, rather than spend the whole semester in a debugging panic that teaches you nothing.
* Be an effective pair programmer.  The partners that you find yourself with during the semester will, mostly, be people you have never met.  The odds are that either they understand the course material significantly better than you, or that you understand the course material significantly better than they do; very rarely will you and your partner be a perfect match in terms of your understanding.  If this happens and they are the ones who understand more, take the time to ask them questions about what is going on in the code that you two are writing; it is *not* a waste of time, and it will help *both* of you to better understand the material.  If you are the one who understands more, be sure to stop periodically and check in with your partner.  Being able to explain the code and the course topics will reinforce your understanding, and might even be fun.
* Become acquainted with sites that contain documentation and Q&A resources, such as Stack Overflow and [Tutorials Point](https://www.tutorialspoint.com/cprogramming/).  They often have very clear examples and explanations of some of the standard library tools you will use.  For example, [this](https://www.tutorialspoint.com/c_standard_library/c_function_sscanf.htm) may be a good place to read about one of the standard library functions you will use in the first lab.
* Be an effective HalliganHelper queue resident.  You will spend a lot of time on the HalliganHelper queue.  Before speaking with a TA, there are a number of steps you should follow:
  * First, you should run your code through a debugger (gdb) and/or valgrind. If you don't know how to use one or both of these tools, it is *absolutely* worth your time to meet with a TA at the beginning of the semester to get an introduction to these tools.  Humans are bad at reasoning about code, so you need to have some idea of what is actually going on in your code.
  * you should search google/stack overflow to the best of your ability
  * you should draw pictures, which will help to clarify both pointer questions and questions about your design (in terms of interactiosn between modules)
  * you should come up with an educated guess for what you believe the answer is, or might be, and why that is the case
  * you should explain to the TA what you have tried already. "My code is broken" and "Why is this segfault happening?" are common statements that a TA hears when they first walk up to a group, but are not helpful places to begin.
* You will be forced to read technical documentation and header (`.h`) files that will be provided to you.  If you run into code or jargon that you don't understand (especially `typedef` related constructs), you should follow the steps above and then talk to a TA if still confused.  Plowing through the confusion is rarely the right thing to do, and will cost you, in some cases, a significant amount of time.
* Learn effective Googling strategies.  For example, googling `site:stackoverflow.com sscanf` will limit your search results to Stack Overflow.
* As long as you try your best during the class, the points will work themselves out in the end. That's why we give vague grades like "Very good", "good", etc.  Don't worry too much about your grades, don't stay in Halligan into the early morning hours, and please stay healthy :)

### Combining Material

* Write test programs.  If you are curious "what would happen if..." or "why is my code doing xyz...", you should change the code, recompile it, and see what changes.
* Look for interesting questions on Stack Overflow's "Related" and "Hot Network Questions" sidebars.  There are a lot of interesting pieces of C trivia to be found by following those links.
* Write your own assembler for UMASM (the assembly language you write in during the last assignment)
* An excellent question asked by a student in COMP 15 one semester:
  * "We learned in lecture that we use a 'class' to store and model state and behavior.  I understand how we store state, because that's just data that we can store in memory.  But how does a class store behavior?"
  * Spend some time thinking about the answer to this question.  The answer reveals a lot of deeper, subtle points about the relationship between code and data.
* Explore other low-level, systems level languages such as Rust.  A good exercise is to implement the Universal Machine in Rust.
* Since the C standard library is so small, implement various data structures or other tools that would be useful to have in a language:
  * Implement various collections (hash tables, sets, etc.)
  * Implement [arbitrary-precision arithmetic](https://en.wikipedia.org/wiki/Arbitrary-precision_arithmetic)
  * Implement a library for precise real number arithmetic (i.e. make it so that 0.1 + 0.2 == 0.3)
* Explore compilation (look for links in the [COMP 105](#comp-105) section).
* Design and implement your own VM
* Optimize your existing solutions, and learn about what kind of low-level optimizations can be made (bit twiddling hacks, inspecting assembly output, etc.)

### Other related material
Comp 40 gives you the tools to explore a large number of other topics:

* [Hardware emulation](https://en.wikipedia.org/wiki/Hardware_emulation)
* Learn about [concurrency](https://en.wikipedia.org/wiki/Concurrency_(computer_science)) and how it works at a low-level
* Go more in-depth with low-level code
  * Read the coolest [stack overflow question](http://stackoverflow.com/questions/11227809/why-is-it-faster-to-process-a-sorted-array-than-an-unsorted-array) ever
  * Low-level security
    * [Buffer overflow attacks](http://heartbleed.com/) (and also read this cool buffer overflow [story](http://www.gamasutra.com/view/feature/194772/))
    * [Return oriented programming](https://en.wikipedia.org/wiki/Return-oriented_programming)
    * [This](https://trailofbits.github.io/ctf/exploits/references/tr-2007-153.pdf) looks to potentially be a good resource for other low-level security exploits.
  * Learn about how potentially life-threatening [bugs](https://around.com/ariane.html) manifest themselves in low-level code
* Go on to explore higher-level languages, like Python, Java, functional languages, etc., using your low-level knowlede to reason about the performance of constructs in these languages.
* Find and contribute to open-source projects! This course gives you the ability to read large amounts of code, familiarize yourself with an existing codebase, and write real code.  Put it to use by giving back to the larger CS community!

### Tufts resources
* There are a lot of very smart undergrad TAs. Talk to them and learn from them.
* Mark Sheldon gets very excited about some of the topics in Comp 40. Stop by his office to chat with him!
* Norman Ramsey designed the class
* Noah Mendelsohn is the [chairman of the internet](http://www.arcanedomain.com/computerwork.html) and is in general incredibly smart; he teaches COMP 40 on alternating semesters with Prof. Sheldon. Talk to him too!
