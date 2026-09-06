# Honest CSP benchmark

This suite compares the same xorshift64* workload in C+, C, C++, and Rust. It
checks that every executable prints the same checksum, performs warm-ups, keeps
every timed sample, and reports median/min/max wall-clock time, one cold compile
time, binary size, commands, compiler versions, and machine details.

Run it from the repository root:

```powershell
csp-bench --runs 7 --warmup 2 --rounds 25000000
```

C+ currently generates C++ and invokes the selected C++ compiler. Its program
runtime is therefore expected to be close to the equivalent C++ program. Its
compile measurement includes both the C+ frontend and C++ backend, so claiming
that C+ is universally “the fastest language” would not be supported by this
benchmark. This is one integer workload, not a complete language ranking.
