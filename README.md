# Shiro-Process-Reporter
Shiro Process Reporter
当前软件由[https://github.com/AlienFamilyHub/ShikenMatrix/tree/4f8d0b1a71cce75f89a7b29ed2e1c3d8294fdf48](https://github.com/AlienFamilyHub/ShikenMatrix/tree/4f8d0b1a71cce75f89a7b29ed2e1c3d8294fdf48)修改而来
# Kizuna

Kizuna 是一个基于 Tauri 的桌面应用程序，使用 Rust + Vue 3 开发。它会监视当前前台活跃窗口信息、系统 SMTC 媒体信息与窗口图标，并将数据上传到服务器。

实现方式参考 [TNXG/ProcessReporterWingo](https://github.com/TNXG/ProcessReporterWingo)，可视为其 Rust + UI 的实现。

## 现状与计划
- [ ] 尝试接入 AI 自动调整动态简介

## 功能特性

- 实时监控前台活跃窗口
- 系统媒体信息（SMTC）读取
- 窗口图标获取
- 自动上传到服务器
- 上传间隔可配置
- 软件名替换规则可配置

## 实现与文档

关于实现原理与设计思路，可参考 [DeepWiki AlienFamilyHub/Kizuna](https://deepwiki.com/AlienFamilyHub/Kizuna)。

## 配置说明

编辑 `config.yml` 文件，或在软件内设置服务器端点和令牌：

## 常见问题

### 网易云音乐不能上报

网易云音乐不使用微软官方的 SMTC 媒体通道上报信息，因此无法被本程序获取。

可通过插件使其通过 SMTC 上报：

- 网易云音乐：[MicroCBer/BetterNCM](https://github.com/MicroCBer/BetterNCM) 与 [BetterNCM/InfinityLink](https://github.com/BetterNCM/InfinityLink) 搭配使用
