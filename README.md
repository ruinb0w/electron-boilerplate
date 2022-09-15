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
// electron.config.js

module.exports = {
  dev: {
    server: "http://localhost:1234"
  }
}
```

### 打包配置

打包时会根据系统自动进行打包

#### 应用图标

推荐图标大小, 注意不同操作系统的图标格式.

- MacOS: .icns
  - 512px x 512px
  - for retina displays: 1024px x 1024px
- Windows: .ico
  - 256px x 256px
- Linux: .png
  - 512px x 512px

以下为 macos 示例:

```
// electron.config.js

module.exports = {
  packagerConfig: {
    icon: "图标路径/ico.icns"
  }
}
```

#### 操作系统配置

不同操作系统打包配置有所不同, 详见[makers](https://www.electronforge.io/config/makers). 以下是 macos 的示例:

```
// electron.config.js

module.exports = {
  makers: [
    {
        name: "@electron-forge/maker-dmg",
    }
  ]
}
```

#### 页面配置

页面配置有两种方式, 一种是将页面托管在服务器上, 一种是将页面放在本地, 即 app 中.

1. 页面托管在服务器

```
// electron.config.js

module.exports = {
  pro: {
    server: "页面地址"
  }
}
```

2. 页面放在本地(app 中)

将打包好的页面内容放到 `render` 目录下, 注意不要删除 `preload.js`
