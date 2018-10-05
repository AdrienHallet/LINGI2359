# First drafts on the content of the survey
Let's try to be exhaustive here. It's better to have too much and scrap than be short and bullshit ;)
Obviously Work in Progress, feel free to modify

#### Introduction
* What is Symbolic Execution
* How is it useful / used in the software engineering context
  * Maybe use the comparison to unit testing and its lack of completeness

#### The principle
* Preamble on the needed terms and concepts (paths, atomic instruction, ...) whatever we need to explain in the symbolic execution concept.
* Concrete explanation of symbols
* How we use symbols in the symbolic execution
* Where can we use it (almost everywhere ? Can we find an example where symbolic execution cannot be used ?)
  * Softwares
  * Compilers (KLEE is a concolic (concrete/symbolic) tool that can be used on top of the LLVM Compiler Infrastructure Project )
  * Hardware
  * Websites

#### Methods
* Bottom-Up (backward) execution (from the path's end to the program entry point)
* Mixing concrete and symbolic execution (could be moved to a "more methods" section, it's not a pure symbolic execution method per se)
* Using randomly generated inputs to infer the symbol constraints (that's what the DART framework does)

#### Tools and languages
It seems that there are "big" symbolic execution frameworks/principles/algorithms. And these have multiple implementations for one or multiple languages, often build on top of each other. In my research I did not find a link between a type of symbolic execution and its language, which seems fine according to the Church-Turing thesis (this is just a supposition).

* Java : PathFinder (used in SQA), jCUTE (jCUTE is DART for java)
* C : EXE (is quite unique because a lot of frameworks use untyped bytes, EXE is typed and provides what is explained as "bit-level accuracy", can prevent more memory errors), DART (https://web.eecs.umich.edu/~weimerw/2011-6610/reading/p213-godefroid.pdf), CREST (can also detect SQL injections ?)
* Assembly and approx everything (Microsoft) : SAGE (https://patricegodefroid.github.io/public_psfiles/cacm2012.pdf)
* .NET : PEX, since Visual Studio 2010 (thx Microsoft again)
