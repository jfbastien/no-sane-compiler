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
[jfbastien.github.io/no-sane-compiler](https://jfbastien.github.io/no-sane-compiler) (press **S** for speaker notes, use **←** and **→** to navigate backward / forward).

## Video

The talk was given at [CppCon 2016](https://cppcon2016.sched.org/speaker/jfb_) and is [available on YouTube](https://youtu.be/IB57wIf9W1k).

It was previously given at [C++Now 2016](http://cppnow.org/program-2016), is also [on YouTube](https://youtu.be/igLZkoeTPgA) but the recording isn't great.

## References

A (non-comprehensive) list of references that went into creating this talk.

* [No sane compiler would optimize atomics](http://wg21.link/n4455)
* [When should compilers optimize atomics?](http://open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0062r0.html)
* [Agner's Software optimization resources](http://www.agner.org/optimize/)
* [Can Seqlocks Get Along With Programming Language Memory Models?](http://www.hpl.hp.com/techreports/2012/HPL-2012-68.pdf)
* [C/C++11 mappings to processors](https://www.cl.cam.ac.uk/~pes20/cpp/cpp0xmappings.html)
* [Mathematizing C++ Concurrency](https://www.cl.cam.ac.uk/~mjb220/popl085ap-sewell.pdf)
* [Threads Cannot be Implemented as a Library](http://www.hpl.hp.com/techreports/2004/HPL-2004-209.pdf)
* [Common Compiler Optimisations are Invalid in the C11 Memory Model and what we can do about it](http://www.di.ens.fr/~zappa/readings/c11comp.pdf)
* [ARM Barrier Litmus Tests and Cookbook](http://infocenter.arm.com/help/topic/com.arm.doc.genc007826/Barrier_Litmus_Tests_and_Cookbook_A08.pdf)
* [DR 476 (C volatile)](http://www.open-std.org/jtc1/sc22/wg14/www/docs/summary.htm#dr_476)
* [CVE-2015-8550 paravirtualized drivers incautious about shared memory contents](http://xenbits.xen.org/xsa/advisory-155.html)
* [Compiler-Introduced Double-Fetch Vulnerabilities – Understanding XSA-155](http://tkeetch.co.uk/blog/?p=58)
* [GCC Xtensa Options](https://gcc.gnu.org/onlinedocs/gcc-4.8.1/gcc/Xtensa-Options.html)
* [MSVC volatile (C++)](https://msdn.microsoft.com/en-us/library/12a04hfd.aspx)
* [Volatile: Almost Useless for Multi-Threaded Programming](https://software.intel.com/en-us/blogs/2007/11/30/volatile-almost-useless-for-multi-threaded-programming)
* [Should volatile Acquire Atomicity and Thread Visibility Semantics?](http://wg21.link/n2016)
* [Acquire and Release Fences](http://preshing.com/20130922/acquire-and-release-fences/)
* [LKML Memory corruption due to word sharing (Linus Torvalds)](https://gcc.gnu.org/ml/gcc/2012-02/msg00027.html)
* [LKML Memory corruption due to word sharing (Hans Boehm)](https://gcc.gnu.org/ml/gcc/2012-02/msg00037.html)
* [JVM pipeline blog](https://blogs.oracle.com/dave/resource/NHM-Pipeline-Blog-V2.txt)
* [Memory Model for Multithreaded C++](http://www.hboehm.info/c++mm/mmissues.pdf)
* [Atomicity and Visibility in Tiny Embedded Systems](https://www.cs.utah.edu/~regehr/papers/plos06b.pdf)
* [Programming with Threads: Questions Frequently Asked by C and C++ Programmers](http://www.hboehm.info/c++mm/user-faq.html)
* [Hogwild!: A Lock-Free Approach to Parallelizing Stochastic Gradient Descent](http://arxiv.org/pdf/1106.5730v2.pdf)
* [GCC Built-in Functions for Memory Model Aware Atomic Operations](https://gcc.gnu.org/onlinedocs/gcc-6.1.0/gcc/_005f_005fatomic-Builtins.html#_005f_005fatomic-Builtins)
* [GCC Legacy __sync Built-in Functions for Atomic Memory Access](https://gcc.gnu.org/onlinedocs/gcc-6.1.0/gcc/_005f_005fsync-Builtins.html#_005f_005fsync-Builtins)
* [libc++ atomic](https://github.com/llvm-mirror/libcxx/blob/master/include/atomic)
* [compiler-rt atomic](https://github.com/llvm-mirror/compiler-rt/blob/master/lib/builtins/atomic.c)
* [clang CGAtomic](https://github.com/llvm-mirror/clang/blob/master/lib/CodeGen/CGAtomic.cpp)
* [LLVM atomics](http://llvm.org/docs/Atomics.html)

## Meta

Built using [reveal.js](http://lab.hakim.se/reveal-js).
