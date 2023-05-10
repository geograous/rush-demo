### 前提条件

node 版本要求为  `>=12.13.0 <13.0.0 || >=14.15.0 <15.0.0 || >=16.13.0 <17.0.0 || >=18.0.0`

- 安装 rush `npm install -g @microsoft/rush`

  

### 运行项目

```shell
# 安装依赖
rush install
# 运行 app1 子项目
cd apps/app1
# 使用 rushx 替换 yarn
rushx dev

```

### 部署项目

1. 执行子项目的部署命令
```shell
# 安装依赖
rush install
# 运行 app1 子项目
cd apps/app1
# 执行子项目中的部署命令
rushx build

```
2. 修改 nginx 配置

### 添加子应用

1. 依次执行以下命令

```shell
# 创建目录
mkdir apps libs
cd apps
# 拷贝现存项目
cp -R ~/my-app/ ./app1
# 删除原来的 git 记录
rm -rf .git
# 删除原来的 shrinkwrap 文件和 git 配置文件
rm -f yarn.lock .npmrc .gitattributes .gitignore

```
2. 修改 rush 配置
在 rush.json 中添加相关配置，其中 projectName 和 package.json 中的 name 保持一致。

3. 执行 rush update

### 注意事项
 - 不要使用 yarn/npm/pnpm 命令，统一使用 rush/rushx
 - yarn 不支持 workspace，如果需要支持，就需要切换成 pnpm
 - 如果遇到问题，大概率是依赖包的问题，推荐删除 node_modules 重新执行 rush update

#### 参考
[rush 文档](https://rushjs.io/zh-cn/pages/intro/welcome/)
