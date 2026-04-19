# entitiesGit

# Gitee

## 第一次提交到 Gitee

- 浏览器登录 gitee.com
- 新建仓库，起一个名字（这就是上面的「你的仓库名」）
- 创建完成后，在仓库页点 「克隆/下载」→ SSH，复制整段地址，那就是你 git remote add origin ... 要用的 URL
```bash
# 切换到对应路径
cd entitiesGit

# 在当前目录建仓库，会生成 .git
git init

# 把已有文件纳入版本控制（大文件、不想提交的可在之前加 .gitignore）
git add .

# 产生第一次提交，否则没有东西可 push
git commit -m "第一次提交，动画，无动画，芙宁娜"

# 绑定 Gitee
git remote add origin git@gitee.com:s-way/entities-git.git

# 把当前分支改名为 main（可选，但和你后面 push main 一致）
git branch -M main

# 生成一对密钥，直接回车1，直接回车2，直接回车3.
ssh-keygen -t ed25519 -C "你的邮箱"

# 把公钥加到 Gitee，会输出内容，全部复制，浏览器打开 Gitee → 头像 → 设置 → SSH 公钥 → 添加公钥 → 粘贴 → 保存。
cat ~/.ssh/id_ed25519.pub

# 推上去并设置上游分支，输入 yes 然后回车
git push -u origin main
```

# 获取 Gitee 某个文件夹/文件的直链

- 直链 = https://gitee.com/所有者/仓库/raw/分支/文件路径
- 举例，文件 = https://gitee.com/s-way/entities-git/raw/main/images/black-and-white-9929839.png

- 直链 = https://gitee.com/所有者/仓库/tree/分支/文件夹路径
- 举例，文件夹 = https://gitee.com/s-way/entities-git/tree/main/images

## 更新仓库内容，提交到 Gitee
```bash

```

# GitHub

## 第一次提交到 GitHub

- 浏览器打开 https://github.com，登录。
- 右上角 New repository 新建仓库（使用默认即可，不要「用 README 初始化」可避免和本地已有提交冲突；若已勾选，首次 push 前可能要先 pull --rebase 或合并）。
- 复制仓库的 SSH 或 HTTPS 地址，例如：git@github.com:你的用户名/仓库名.git
```bash
# 切换到对应路径
cd entitiesGit

# 在当前目录建仓库，会生成 .git
git init

# 把已有文件纳入版本控制（大文件、不想提交的可在之前加 .gitignore）
git add .

# 产生第一次提交，否则没有东西可 push
git commit -m "第一次提交，动画，无动画，芙宁娜"

# 绑定 GitHub
git remote add origin git@github.com:phymodel/entitiesGit.git

# 把当前分支改名为 main（可选，但和你后面 push main 一致）
git branch -M main

# 生成一对密钥，直接回车1，直接回车2，直接回车3.
ssh-keygen -t ed25519 -C "你的邮箱"

# 把公钥加到 GitHub，会输出内容，全部复制，浏览器打开 GitHub → 头像 → 设置 → SSH 公钥 → 添加公钥 → 粘贴 → 保存。
cat ~/.ssh/id_ed25519.pub

# 推上去并设置上游分支，输入 yes 然后回车
git push -u origin main
```