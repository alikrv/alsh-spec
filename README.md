# ALSH Specification repo
This repo contains only specifications ("spec") for ALSH (the programming language)
There are two different ones:
- NORMAL spec
- COMPILER spec

The two have differences and are implemented by alsh-rs, the system shell; and alshc, the compiler for alsh; respectively.
For instance:
Alsh code written as per the NORMAL spec is a lot more chaotic and, as I like to call it, _vibe-based_ than code written as per the COMPILER spec. The latter is more C-like and strictly typed than the first one.

### more info:
ALSH is predominantly a Rust project. Alsh (the shell) is written wholely in Rust;
and the compiler is written _almost_ all in Rust (reuses a lot of alsh (the shell) code, most notably the parser) + a tiny runtime ("the Alsh runtime") in C, which is needed for arena-based allocation and string helpers used by the compiler.
_(the alsh runtime is not something big as the name would suggest, and is inside of the alshc repo)_