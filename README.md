# What is this repo?

This repository is a resource for Tufts Computer Science students who are
interested in learning more about the classes they are currently taking.

# What classes are there?

* [COMP 105](#comp-105)

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
