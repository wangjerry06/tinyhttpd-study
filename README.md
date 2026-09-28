# tinyhttpd-study

> 我的学习仓库：从 0 开始读懂并魔改 Tinyhttpd（不到 500 行的超轻量 HTTP 服务器）

## 这是什么

这是我的网络编程练手项目第一站。原版 [Tinyhttpd](https://github.com/EZLippi/Tinyhttpd)
（J. David Blackstone 写于 1999 年，中文注释版由 EZLippi 维护）是一个不到 500 行的 C 语言
HTTP 服务器——小到能一个下午通读，却五脏俱全：socket、多进程、HTTP 解析、CGI。

我的目标不是"看懂"，而是"改写"：

- [ ] 通读源码，输出阅读笔记（`notes/`）
- [ ] 本地跑通，用浏览器 + curl 验证 CGI
- [ ] 魔改一：把 HTTP 解析用 C++ 重写（练 RAII / std::string）
- [ ] 魔改二：原版只支持 GET，加上 POST
- [ ] 魔改三：原版每个请求 fork 一个进程，尝试改为线程模型
- [ ] （可选）压测对比：进程模型 vs 线程模型

## 目录结构

```
tinyhttpd-study/
├── original/    # 原版源码（未改动，保留原 LICENSE）
├── notes/       # 学习笔记（源码阅读、踩坑记录）
├── rewrite/     # 我的改写版本（C++ 重写 / 新特性）
└── README.md
```

## 进度日志

| 日期 | 事项 |
|------|------|
| 2026-09-28 | 建仓，导入原版源码，制定学习计划 |

## 致谢与许可

- 原作者：J. David Blackstone（Tinyhttpd）
- 中文注释版：[EZLippi/Tinyhttpd](https://github.com/EZLippi/Tinyhttpd)
- `original/` 目录下的代码版权归原作者所有，本仓库学习用途
