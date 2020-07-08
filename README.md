# UnixBench

<!-- vim-markdown-toc GitLab -->

- [Question](#question)
- [route](#route)
- [TODO](#todo)
- [让问题被分析更加广泛一点吧!](#让问题被分析更加广泛一点吧)
- [report A](#report-a)
- [report B](#report-b)

<!-- vim-markdown-toc -->

## Question
<!-- [ ] 为什么龙梦的内核不给龙芯使用，我似乎之前是看到了 龙梦给 5.7 的内核提交过 grep 一下 lomote 的提交。-->
<!-- [ ] 不升级内核必然是遇到问题了，主要遇到的问题是什么。-->

## route
- [ ] 让机器跑起来，复现结果
    - [ ] 之前的测试环境是什么 ?
- [ ] 理解 UnixBench 的源代码
- [ ] 整理现代 trace perf 工具可以实现什么，不可以实现什么
- [ ] 加快调试的方法

## TODO
1. 写一个脚本，让本地本地电脑的测试可以自动部署到4000上
2. 是否存在更快的安装方法 ?
3. 能不能在 x86 的机器上编译，然后传输到机器上运行

## 让问题被分析更加广泛一点吧!
- [ ] 工具进行测试 fuzzing, jekens 自动化测试 ?

有没有自动化测试: fuzzer CI/CD， 有没有自动化测试的内容

    - https://blog.cloudflare.com/a-gentle-introduction-to-linux-kernel-fuzzing/
    - https://github.com/google/syzkaller



## report A
之前看的各种调试，都是在环境搭建的好的情况下使用，现在遇到两个问题:
1. 4000目前只是成功开机过一次，开机之后使用正常
2. 试图在x86笔记本上安装3.10的内核，进入到 grub 界面之后，无法启动，但是使用完全相同的方法，编译5.7内核，可以启动。
针对于这两种情况，是否存在有效的解决办法 ?

解决方法:
1. 金手指
2. KVM

## report B
