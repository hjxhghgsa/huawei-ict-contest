# 华为ICT大赛 · 备赛代码库

第十一届华为ICT大赛（2026-2027 赛季）备赛代码与资料仓库。
主攻 **网络赛道 + 基础软件赛道**，配套在线资料库练习台（WorkBuddy 资料库「练习台」节点）。

## 目录结构

```
华为ICT备赛代码库/
├── eNSP/          # 路由交换 / 无线 / 安全 实验（.topo + 配置 + 抓包 + 结论）
├── python/        # 基础软件赛道：Python 练习（基础语法 / 判断循环 / 函数 / 文件 / 网络编程 / 运维）
├── notes/         # 学习笔记（Markdown，按赛道分）
├── labs/          # 实验实操 22 个（对应资料库实验手册）
├── resources/     # 参考资料 / 题库导出 / 速查表（大文件勿入仓）
├── scripts/       # 辅助脚本（批量处理、配置生成、校验）
└── .gitignore
```

## 规范

- **一个知识点 / 一个实验 = 一个文件夹**，命名 `NN-主题`（如 `02-STP生成树`）。
- 每个文件夹放 `README.md` 写说明、结论、排错记录；代码 / 配置放同目录或子目录。
- 提交信息用中文、讲清"改了什么、为什么"，例如：
  `feat(eNSP): 完成 VLAN 与 Trunk 实验配置与结论`
  `fix(python): 修正判断与循环练习题第3题边界条件`
  `docs(notes): 补充 OSPF 邻居建立排查笔记`
- 大文件（>50MB 的镜像、安装包）**不要进仓库**，放网盘并在 `resources/README.md` 记链接。

## 与在线资料库的关系

- 在线练习台（`workbuddy.link/p/wHQXYffnPtRJRghYY7sphE`）是用来**练**的。
- 本仓库是用来**存代码和沉淀笔记**的，互为备份。
- 备赛专区子页（`workbuddy.link/p/ngLDYd7D9GL99zTJpgiTV8`）里有 5 个模块，对应本仓库的
  `notes/`、`eNSP/`、`python/`、`labs/`。

## 推到 Gitee（待办）

本仓库已 `git init` 并完成首次提交，但**尚未关联远程**。要推到 Gitee：

1. 在 gitee.com 新建一个**空仓库**（不要勾选自动生成 README/.gitignore）。
2. 复制仓库 HTTPS 地址，执行：
   ```bash
   git remote add origin https://gitee.com/<你的用户名>/<仓库名>.git
   git push -u origin master
   ```
3. 私有仓库推送需要 Gitee **私人令牌（token）** 或账号密码；
   若要我帮你推，给我 Gitee 用户名 + 私人令牌即可（令牌只在本次推送用，用完即删）。
