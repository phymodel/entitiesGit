# entity-3d

# Gitee
- 浏览器登录 gitee.com
- 新建仓库，起一个名字（这就是上面的「你的仓库名」）
- 创建完成后，在仓库页点 「克隆/下载」→ SSH，复制整段地址，那就是你 git remote add origin ... 要用的 URL
```bash
# 在当前目录建仓库，会生成 .git
git init
# 把已有文件纳入版本控制（大文件、不想提交的可在之前加 .gitignore）
git add .
# 产生第一次提交，否则没有东西可 push
git commit -m "你的说明"
# 绑定 Gitee
git remote add origin git@gitee.com:s-way/entities-git.git
# 把当前分支改名为 main（可选，但和你后面 push main 一致）
git branch -M main
# 推上去并设置上游分支
git push -u origin main
```

# GitHub