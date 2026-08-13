# GitHub 仓库创建与推送指南

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

## 日常使用

### 提交学习记录

每次学习后，将笔记和代码放入对应目录，然后：

```bash
# 查看改动
git status

# 添加所有改动
git add -A

# 提交
git commit -m "docs: 完成数字逻辑基础笔记"

# 推送
git push
```

### 推荐的 commit message 前缀

| 前缀 | 用途 | 示例 |
|:---:|------|------|
| `docs:` | 笔记/文档更新 | `docs: 添加 RV32I 指令格式笔记` |
| `feat:` | 新功能/新代码 | `feat: 实现 ALU 模块` |
| `fix:` | 修复 bug | `fix: 修复流水线转发逻辑错误` |
| `test:` | 添加测试 | `test: 添加 CPU 指令级测试` |
| `chore:` | 杂项维护 | `chore: 更新 .gitignore` |

## 给导师看时的小建议

1. **README 是门面**：保持 README 中的进度表更新，让导师一眼看到你的学习阶段
2. **commit 历史是证明**：保持规律的提交频率，体现持续学习的态度
3. **笔记要清晰**：用自己的话总结，展示理解深度而非复制粘贴
4. **代码要能跑**：确保代码目录中的实现是经过仿真验证的
5. **波形截图**：在 simulation/waves/ 中保存关键仿真波形截图，直观展示成果

---

*如有问题，可参考 [GitHub 官方文档](https://docs.github.com/zh/repositories)。*
