# electron-boilerplate

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

## Build

### 页面托管在服务器

```
module.exports = {
  dev: {
    server: "页面地址"
  }
}
```

### 页面放在本地(app 中)

将打包好的页面内容放到 `render` 目录下, 注意不要删除 `preload.js`
