# 华为ICT大赛 · 备赛代码库

第十一届华为ICT大赛（2026-2027 赛季）备赛代码与资料仓库，主攻 **网络赛道 + 基础软件赛道**。
本仓库用于沉淀实验配置、练习代码与学习笔记，配合在线练习台互为备份。

---

## 一、项目要解决的问题

备赛过程中资料散落在各处（eNSP 拓扑、Python 练习、笔记、实验手册），容易丢失且难以复盘。
本项目把备赛内容按"一个知识点 / 一个实验 = 一个文件夹"的规范统一收纳，提供：

- 一套可版本化、可复盘的备赛资料结构；
- 网络赛道（路由交换 / 无线 / 安全）与基础软件赛道（Python）的练习骨架；
- 与在线练习台互通的本地沉淀库，断网也能复习。

> 说明：本仓库是**学习沉淀库**，不是考试答案；涉及账号、令牌等凭据请放本地，切勿提交（见 `.gitignore`）。

---

## 二、主要功能

| 模块 | 内容 |
| --- | --- |
| `eNSP/` | 路由交换 / 无线 / 安全 实验（`.topo` 拓扑 + 配置 + 抓包 + 结论），含 VLAN/Trunk、STP、静态路由与 OSPF、ACL/NAT、WLAN、防火墙 |
| `python/` | 基础软件赛道 Python 练习：基础语法、判断与循环、函数与模块、文件与字符串、网络编程、自动化与运维 |
| `notes/` | 按赛道分类的学习笔记（Markdown） |
| `labs/` | 实验实操（对应在线实验手册） |
| `resources/` | 参考资料 / 题库导出 / 速查表（大文件不进仓，只记链接） |
| `scripts/` | 辅助脚本：批量处理、配置生成、校验 |

---

## 三、安装方法

### 1. 克隆仓库

```bash
git clone https://github.com/hjxhghgsa/huawei-ict-contest.git
cd huawei-ict-contest
```

### 2. 准备本地环境（按需）

- **eNSP 实验**：安装华为 eNSP + VirtualBox + 对应设备镜像（ENSP、CE、USG 等），用于打开 `eNSP/` 下的 `.topo` 文件。
- **Python 练习**：建议 Python 3.12+，勾选 `Add Python to PATH`。

  ```bash
  python --version        # 确认 3.12+
  pip install -r python/requirements.txt   # 若某子目录提供依赖清单
  ```

- **笔记 / 资料**：纯 Markdown，任意编辑器（VS Code / Obsidian / Typora）即可阅读。

### 3. 凭据与隐私

仓库已通过 `.gitignore` 忽略 `*.token`、`*.secret`、`.env`、`gitee_token.txt` 等文件。
**请勿把私人令牌、账号密码写进任何会被提交的文件。**

---

## 四、使用示例

### 打开一个 eNSP 实验

```text
1. 进入 eNSP/03-静态路由与OSPF
2. 双击其中的 .topo 文件用 eNSP 打开
3. 按 README.md 里的步骤配置、抓包、记录结论
```

### 运行一个 Python 练习

```bash
cd python/01-基础语法与数据类型
python hello.py          # 把示例跑通，再照着改
```

### 新增一个知识点 / 实验

```text
规则：一个主题 = 一个文件夹，命名 NN-主题
例：新建 07-BGP，里面放 README.md（说明 + 结论 + 排错）和代码/配置
提交信息用中文讲清"改了什么、为什么"：
  feat(eNSP): 完成 VLAN 与 Trunk 实验配置与结论
  fix(python): 修正判断与循环练习题第3题边界条件
```

---

## 目录结构

```text
华为ICT备赛代码库/
├── eNSP/        # 路由交换 / 无线 / 安全 实验
├── python/      # 基础软件赛道：Python 练习
├── notes/       # 学习笔记（按赛道分）
├── labs/        # 实验实操
├── resources/   # 参考资料 / 题库 / 速查表（大文件勿入仓）
├── scripts/     # 辅助脚本
└── .gitignore
```

## 规范

- **一个知识点 / 一个实验 = 一个文件夹**，命名 `NN-主题`（如 `02-STP生成树`）。
- 每个文件夹放 `README.md` 写说明、结论、排错记录；代码 / 配置放同目录或子目录。
- 提交信息用中文、讲清"改了什么、为什么"。
- 大文件（>50MB 的镜像、安装包）**不要进仓库**，放网盘并在 `resources/README.md` 记链接。

## 许可证

本项目以 [MIT 许可证](./LICENSE) 开源。
