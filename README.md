# No Sane Compiler Would Optimize Atomics

## Abstract

False.

Compilers do optimize atomics, memory accesses around atomics, and utilize
architecture-specific knowledge. My hobby is to encourage compilers to do more
of this, programmers to rely on it, and hardware vendors to give us new atomic
toys to optimize with. Oh, and standardize yet more close-to-the-metal
concurrency and parallelism tools.

But, you say, surely volatile always means volatile, there’s nothing wrong with
my benign races, nothing could even go wrong with non-temporal accesses, and who
needs 6 memory orderings anyways‽ I’m glad you asked, let me tell you about my
hobby…

## Talk Details

This talk is based on a paper I wrote for the C++ standards committee,
[no sane compiler would optimize atomics](http://wg21.link/n4455) (abstract:
`false`). The title and abstract are such perfectly flippant clickbait, yet you
won't believe how there's actual content hiding behind the snark!

View the presentation:
[jfbastien.github.io/no-sane-compiler](https://jfbastien.github.io/no-sane-compiler).

The talk was given at [C++Now 2016](http://cppnow.org/program-2016).

Built using [reveal.js](http://lab.hakim.se/reveal-js).
