<img src="internals/img/erb-banner.png" width="100%" />

<br>

## 1. 安装

- **If you have installation or compilation issues with this project, please see [our debugging guide](https://github.com/electron-react-boilerplate/electron-react-boilerplate/issues/400)**

First, clone the repo via git and install dependencies:

```bash
git clone --depth 1 --single-branch https://github.com/electron-react-boilerplate/electron-react-boilerplate.git your-project-name
cd your-project-name
yarn
```

## 2. 开发

Start the app in the `dev` environment. This starts the renderer process in [**hot-module-replacement**](https://webpack.js.org/guides/hmr-react/) mode and starts a webpack dev server that sends hot updates to the renderer process:

```bash
yarn dev
```

## 3. 打包

To package apps for the local platform:

```bash
yarn package
```

## 4. Docs

See our [docs and guides here](https://electron-react-boilerplate.js.org/docs/installation)

## 5. Adding Dependencies

### `./package.json` 

除了原生模块以外模块

### `./app/package.json` 

负责原生模块

## 6. 配置步骤

### 6.1 修改 webpack.config.base.js 文件,支持 js、jsx

```javascript
      {
        test: /\.tsx?$/,
        exclude: /node_modules/,
        use: {
          loader: 'babel-loader',
          options: {
            cacheDirectory: true,
          },
        },
      },
```

```javascript
      {
        test: /\.(js|mjs|jsx|ts|tsx)$/,
        exclude: /node_modules/,
        use: {
          loader: 'babel-loader',
          options: {
            cacheDirectory: true,
          },
        },
      },
```

