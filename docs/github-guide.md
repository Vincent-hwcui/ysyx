# GitHub 仓库创建与推送指南

> 只想看"每次更新进度该怎么提交"？直接跳到 [日常流程速查](#日常流程速查)。下面是首次建仓库的完整步骤。

## 前置准备

确保已配置 Git 用户名和邮箱：

```bash
git config --global user.name "你的名字"
git config --global user.email "你的邮箱@example.com"
```

## 第一步：在 GitHub 上创建空仓库

1. 打开 [https://github.com/new](https://github.com/new)
2. 填写仓库名称：`ysyx`（或你喜欢的名字）
3. 填写描述：`一生一芯学习记录 - 从数字逻辑到流片的完整历程`
4. 选择 **Public**（公开，这样导师可以查看）
5. **不要**勾选以下选项（仓库已初始化，避免冲突）：
   - ❌ Add a README file
   - ❌ Add .gitignore
   - ❌ Choose a license
6. 点击 **Create repository**

## 第二步：关联远程仓库

将下面的 `你的用户名` 替换为你的 GitHub 用户名：

```bash
cd ysyx

# 添加远程仓库
git remote add origin https://github.com/你的用户名/ysyx.git

# 验证
git remote -v
```

## 第三步：推送到 GitHub

```bash
git push -u origin main
```

首次推送时，Git 会提示输入 GitHub 用户名和密码。**注意：GitHub 已不支持密码认证**，需要使用 Personal Access Token (PAT)。

### 创建 Personal Access Token

1. 打开 [https://github.com/settings/tokens](https://github.com/settings/tokens)
2. 点击 **Generate new token (classic)**
3. 填写 Note：`git push`
4. 勾选 **repo** 权限
5. 点击 **Generate token**
6. **复制生成的 token**（只显示一次！）
7. 推送时用户名填 GitHub 用户名，密码粘贴 token

## 第四步：验证

打开你的 GitHub 仓库页面，确认所有文件已上传。

## 第五步：添加仓库 Topics（可选，提升可见性）

在 GitHub 仓库页面点击设置图标添加 Topics：
- `risc-v`
- `cpu-design`
- `chip-design`
- `verilog`
- `ysyx`
- `learning-notes`

## 日常流程速查

每次更新学习进度都按这四条走。先进入仓库目录：

```bash
cd "C:\Users\17329\WorkBuddy\2026-08-13-15-26-11\ysyx"
```

然后：

```bash
git status                          # 1. 看改了哪些文件
git add -A                          # 2. 把改动放进待提交区
git commit -m "docs: 更新 F3 进度"   # 3. 记录一次快照
git push                            # 4. 推到 GitHub
```

每条命令在做什么：

1）`git status` 列出所有改动过的文件。**提交前一定要扫一眼**，防止把编译产物、自动保存文件之类不该提交的东西带上。
2）`git add -A` 把改动放进待提交区。只想提交某一个文件时，换成 `git add 文件路径`，比如 `git add logs/progress.md`。
3）`git commit -m "..."` 正式记录一次快照。message 的写法见下面那张表。
4）`git push` 推到 GitHub。**只 commit 不 push 的话，远程仓库上什么都没有**，助教也看不到。

一次 commit 只讲一件事。可以连续做多轮 add + commit，比如先提交笔记、再提交代码，这样 `git log` 读起来清楚得多。

### 第一次推送会要求登录

本机已经配好了 Git Credential Manager（凭证助手 = manager），所以**不需要自己建 Personal Access Token**：

`git push` 时会自动弹出浏览器窗口，登录 GitHub 账号并点授权，窗口自己关掉就算成功，之后会永久记住，不用再登录。

如果弹出的不是浏览器，而是终端里的 `Username / Password` 提示，说明走了另一条认证路径：

1）Username 填 GitHub 用户名（Qiaomao39）
2）Password **不能填 GitHub 登录密码**，要填 Personal Access Token
3）Token 生成地址：<https://github.com/settings/tokens> → Generate new token (classic) → 勾选 `repo` → 生成后立刻复制（只显示一次）

### 改错了怎么退

```bash
git restore 文件名                # 撤销这个文件还没 add 的修改
git restore --staged 文件名       # 把它从待提交区拿出来（改动本身还在）
git log --oneline -10             # 看最近 10 次提交
git diff                          # 看还没 add 的具体改动内容
git diff --staged                 # 看已经 add、即将提交的改动内容
```

### 推荐的 commit message 前缀

格式统一为 `前缀: 做了什么`，一行说清。

| 前缀 | 用途 | 示例 |
|:---:|------|------|
| `docs:` | 笔记/文档/进度日志 | `docs: 更新 F3 进度日志` |
| `feat:` | 新功能/新代码 | `feat: 实现 ALU 模块` |
| `fix:` | 修复 bug | `fix: 修复流水线转发逻辑错误` |
| `test:` | 添加测试 | `test: 添加 CPU 指令级测试` |
| `chore:` | 杂项维护 | `chore: 更新 .gitignore` |
| `F/E/D/C/B/A/S:` | 某阶段的任务产出 | `F3: 完成 3-8 译码器` |

阶段号那一行是给"一生一芯"用的：助教看 `git log` 就是看你在推进哪个阶段，所以电路、笔记这类产出最好带上阶段号。

## 给导师看时的小建议

1. **README 是门面**：保持 README 中的进度表更新，让导师一眼看到你的学习阶段
2. **commit 历史是证明**：保持规律的提交频率，体现持续学习的态度
3. **笔记要清晰**：用自己的话总结，展示理解深度而非复制粘贴
4. **代码要能跑**：确保代码目录中的实现是经过仿真验证的
5. **波形截图**：在 simulation/waves/ 中保存关键仿真波形截图，直观展示成果

---

*如有问题，可参考 [GitHub 官方文档](https://docs.github.com/zh/repositories)。*
