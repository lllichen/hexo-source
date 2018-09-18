---
title: garbage_collection
date: 2018-08-20 14:54:24
tags: java 
---

## ConcurrentMarkSweep (CMS)

CMS 垃圾回收分6个阶段

1. 初始标记（STW)
2. 并发标记
3. 预清理
4. 重新标记（STW）
5. 并发清理
6. 并发重置

初始标记和重新标记会会独占jvm虚拟机，其余是和工作线程并发执行的，CMS虚拟机会有效降低程序的卡顿。