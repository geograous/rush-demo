
### 添加新项目

```
mkdir apps libs
cd apps
cp -R ~/my-app/ ./app1
rm -rf .git
rm -f yarn.lock .npmrc .gitattributes .gitignore

```

修改 package.json 中的 name