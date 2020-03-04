---
title: 解决vs code 因为在此系统上禁止运行脚本 报错
date: 2020-02-27 09:15:08
tags: 前端
categories: vscode
---


# 解决vs code 因为在此系统上禁止运行脚本 报错


今天想在VScode中直接运行 hexo s 结果发现VScode显示 此系统上禁止运行脚本  解决方法如下
<!--more-->

## 以管理员身份打开VS Code 打开终端
## 查看ExecutionPolicy状态

> 输入 get-ExecutionPolicy 显示Restricted 说明在终端中禁止运行脚本

## 修改ExecutionPolicy
> set-ExecutionPolicy

## 设置值
> RemoteSigned

## 验证状态
> get-ExecutionPolicy

---

## 下面是执行结果

    PS D:\blog\hexo> get-ExecutionPolicy
    Restricted
    PS D:\blog\hexo> set-ExecutionPolicy

    位于命令管道位置 1 的 cmdlet Set-ExecutionPolicy
    请为以下参数提供值:
    ExecutionPolicy: RemoteSigned
    PS D:\blog\hexo> get-ExecutionPolicy
    RemoteSigned
    PS D:\blog\hexo> hexo s  
    INFO  Start processing
    INFO  Hexo is running at http://localhost:4000 . Press Ctrl+C to stop.
