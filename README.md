# Community-workshop-downloader

Desktop app to download anonymously allowed workshop items.

# The below is guide of template of electron.js which is used to build this project

## Overview

📦 Out of the box
🎯 Based on [react-ts](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) template, less invasive
🌱 Simple directory structure，real flexible
💪 Support Use Electron、Node.js API and in Renderer-process
🔩 Support C/C++ native addons
🖥 It's easy to implement multiple windows

## Quick start

```sh
npm create electron-vite
```

![electron-vite-react.gif](https://github.com/electron-vite/electron-vite-react/blob/main/public/electron-vite-react.gif?raw=true)

## Debug

![electron-vite-react-debug.gif](https://github.com/electron-vite/electron-vite-react/blob/main/public/electron-vite-react-debug.gif?raw=true)

## Directory structure

_🚨 By default, the files in `electron` folder will be built into the `dist/electron`_

```tree
├── electron                  Electron-related code
│   ├── main                  Main-process source code
│   ├── preload               Preload-script source code
│   └── resources             Resources for the production build
│       ├── icon.icns             Icon for the application on macOS
│       ├── icon.ico              Icon for the application
│       ├── installerIcon.ico     Icon for the application installer
│       └── uninstallerIcon.ico   Icon for the application uninstaller
│
├── release                   Generated after production build, contains executables
│   └──{version}
│       ├── {os}-unpacked     Contains unpacked application executable
│       └── Setup.{ext}       Installer for the application
│
├── public                    Static assets
└── src                       Renderer source code, your React application
```

## `dependencies` vs `devDependencies`

The easiest way

- Put Node.js packages in `dependencies`
- Put web packages in `devDependencies`

see more 👉 [dependencies vs devDependencies](https://github.com/electron-vite/vite-plugin-electron-renderer#dependencies-vs-devdependencies)

<!--
- First, you need to know if your dependencies are needed after the application is packaged.

- Like [serialport](https://www.npmjs.com/package/serialport), [sqlite3](https://www.npmjs.com/package/sqlite3) they are node-native modules and should be placed in `dependencies`. In addition, Vite will not build them, but treat them as external modules.

- Dependencies like [Vue](https://www.npmjs.com/package/vue) and [React](https://www.npmjs.com/package/react), which are pure javascript modules that can be built with Vite, can be placed in `devDependencies`. This reduces the size of the application.
-->
