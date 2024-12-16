---
layout: post
title: 'GitHub 加速（亲测有效）'
date: 2024-12-16
author: Afan
cover: 'https://cdn.luogu.com.cn/upload/image_hosting/mugcc3dj.png'
tags: GitHub
---

GitHub 打不开或者是访问速度慢主要是因为时间都花在解析 DNS 上面了。

那怎么解决呢？不用挂梯子也可以，虽然没有梯子效果好，但至少要比原来好多了。

1. 在电脑的搜索页面找的记事本
2. 右键选择“以管理员身份运行”
3. 点击“文件”
4. 点击“打开”
5. 打开路径 `C:\Windows\System32\drivers\etc`
6. 选择文件 `hosts`（老电脑没有此文件请选择文件 `networks`）
7. 在最后一行加上：
   ```text
   20.205.243.166 github.com
   140.82.112.4 github.com
   151.101.1.6 github.global.ssl.fastly.net
   185.199.108.153 assets-cdn.github.com
   185.199.109.153 assets-cdn.github.com
   185.199.110.153 assets-cdn.github.com
   185.199.111.153 assets-cdn.github.com
   ```
8. 打开 `cmd.exe`（命令提示符）
9. 运行 `ipconfig /flushdns` 指令

接着再打开 [GitHub](https://github.com/) 就好了。
