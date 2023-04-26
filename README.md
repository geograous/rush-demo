
### 添加新项目

```
mkdir apps libs
cd apps
cp -R ~/my-app/ ./app1
rm -rf .git
rm -f yarn.lock .npmrc .gitattributes .gitignore

```

在 rush.json 中添加相关配置，其中 projectName 和 package.json 中的 name 保持一致。
