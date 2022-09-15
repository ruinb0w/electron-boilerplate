# electron-boilerplate

## Start

> 如果使用 vue,react 等框架需要先进行**Config-开发配置**

使用以下命令即可启动项目

```
npm start
```

## Build

> 打包前需要根据需要进行配置

使用以下命令即可进行打包

```
npm run make
```

## Config

配置都放在`electron.config.js`中

### 开发配置

指定开发时页面本地服务的地址

```
module.exports = {
  dev: {
    server: "http://localhost:1234"
  }
}
```

### 打包配置

#### 页面配置

页面配置有两种方式, 一种是将页面托管在服务器上, 一种是将页面放在本地, 即 app 中.

1. 页面托管在服务器

```
module.exports = {
  dev: {
    server: "页面地址"
  }
}
```

2. 页面放在本地(app 中)

将打包好的页面内容放到 `render` 目录下, 注意不要删除 `preload.js`
