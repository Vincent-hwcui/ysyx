# GitHub 使用记录

上面是第一次建仓库的过程（已完成，留作备查），下面是每次提交进度的流程。

## 仓库的基本情况

仓库在 <https://github.com/Vincent-hwcui/ysyx>，公开，用的是 MIT 协议，默认分支 `main`。

本机的 git 配置：`user.name` 是 Vincent-hwcui，`user.email` 是 1732951162@qq.com（这个邮箱在 GitHub 账号里验证过，提交能正确关联到账号上）。凭证助手设成了 `manager`，也就是 Git Credential Manager。

## 当时建仓库的步骤（备查）

先在 GitHub 上新建一个空仓库，名字 `ysyx`，选 Public；**README、.gitignore、LICENSE 都不要勾**，因为这个项目是本地先写好再推的，勾了会产生冲突。建完把本地目录和远程关联起来：

```bash
git remote add origin https://github.com/Vincent-hwcui/ysyx.git
git remote -v          # 确认一下
git push -u origin main
```

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

1）`git status` 列出所有改动过的文件。**提交前一定要扫一眼**，防止把编译产物、Logisim 的 `.autosave` 之类不该提交的东西带上。
2）`git add -A` 把改动放进待提交区。只想提交某一个文件时换成 `git add 文件路径`，比如 `git add logs/progress.md`。
3）`git commit -m "..."` 正式记录一次快照，message 的写法见下面那张表。
4）`git push` 推到 GitHub。**只 commit 不 push 的话远程仓库上什么都没有**，助教也看不到。

一次 commit 只做一件事。可以连续做几轮 add 和 commit，比如先提交笔记再提交电路，这样 `git log` 读起来清楚。

### 第一次推送会要求登录

本机的凭证助手是 Git Credential Manager，所以**不需要自己建 Personal Access Token**：`git push` 的时候会自动弹出浏览器窗口，登录 GitHub 账号点一下授权，窗口自己关掉就算成功，之后会一直记住，不用重复登录。

如果弹出来的不是浏览器而是终端里的 `Username / Password` 提示，说明走了另一条认证路径。这时候 Username 填 GitHub 用户名 `Vincent-hwcui`，Password 不能填登录密码、要填 Token，Token 在 <https://github.com/settings/tokens> 生成（选 classic，勾 `repo`），生成后立刻复制，只显示这一次。

### 改错了怎么退

```bash
git restore 文件名                # 撤销这个文件还没 add 的修改
git restore --staged 文件名       # 把它从待提交区拿出来（改动本身还在）
git log --oneline -10             # 看最近 10 次提交
git diff                          # 看还没 add 的具体改动内容
git diff --staged                 # 看已经 add、即将提交的改动内容
```

### commit message 怎么写

格式统一成 `前缀: 做了什么`，一行说清。

| 前缀 | 用途 | 示例 |
|:---:|---|---|
| `docs:` | 笔记、文档、进度日志 | `docs: 更新 F3 进度日志` |
| `feat:` | 新增电路或代码 | `feat: 新增 3-8 译码器` |
| `fix:` | 修 bug | `fix: 修正 N 管源漏接反的问题` |
| `test:` | 加测试 | `test: 补 4-16 译码器的真值表` |
| `chore:` | 杂项维护 | `chore: 更新 .gitignore` |

后面可以带上阶段号，比如 `feat(f3): 新增七段数码管译码器`，这样在 `git log` 里一眼能看出是在推进哪个阶段。助教看提交记录主要就是看这个。

## 两个容易忘的点

一是推之前先 `git status` 扫一眼，桌面上那些临时文件、`index-1.html` 这种预览产物别一起带上去。

二是在 Windows 的 cmd 里敲 git 命令时，先执行 `chcp 65001` 把编码切成 UTF-8，否则中文 commit message 会按 GBK 存进去，在 GitHub 上看是乱码。
