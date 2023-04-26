### 前提条件

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

#### 参考
[rush 文档](https://rushjs.io/zh-cn/pages/intro/welcome/)
