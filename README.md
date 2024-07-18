1.安装nvm-window（一般情况下会安装多个版本的nodejs，例如14/16/18）

| 步骤或操作          | 地址                                                         | 备注                                                     |
| -------------- | ------------------------------------------------------------ |--------------------------------------------------------|
| 1.安装nvm-setup.exe | 下载地址：https://github.com/coreybutler/nvm-windows/releases | 下载最新版                                                  |
| 2.配置nvm镜像地址   | 修改安装目录中的settings.txt<br />root: C:\Program Files\nvm<br/>path: C:\Program Files\nodejs<br/>node_mirror: https://npmmirror.com/mirrors/node/<br/>npm_mirror: https://npmmirror.com/mirrors/npm/ | 默认是国外地址，下载极有可能失败<br />nvm默认安装目录可能是C:\Program Files\nvm |
| nvm install 18 | https://nodejs.org/en/download/releases                      | 只写大版本号会直接安装该大版本号的最新版本，例如14/16/18      |

具体说明详见这个链接：https://www.cnblogs.com/gaozejie/p/10689742.html

2.npm地址配置

| 操作                                                         | 输出                        | 备注                                         |
| ------------------------------------------------------------ | --------------------------- | -------------------------------------------- |
| npm config get registry                                      | https://registry.npmjs.org/ | 查看当前设定的源地址                         |
| npm config set registry https://registry.npmmirror.com/      |                             | 修改成国内淘宝源的地址                       |
| npm config set sass_binary_site https://registry.npmmirror.com/binary.html?path=node-sass/ |                             | 修改下载node-sass（一个css预处理器）的下载源 |

3.yarn配置（用于vue2项目）（可选）

| 操作                                                        | 输出                         | 备注                   |
| ----------------------------------------------------------- | ---------------------------- | ---------------------- |
| npm install -g yarn                                         |                              | 全局安装yarn           |
| yarn config get registry                                    | https://registry.yarnpkg.com | 查看当前设定的源地址   |
| yarn config set registry https://registry.npmmirror.com/ -g |                              | 修改成国内淘宝源的地址 |

4.pnpm配置（用于vue3项目）（可选）

| 操作                     | 输出                            | 备注                                        |
| ------------------------ | ------------------------------- | ------------------------------------------- |
| npm install -g pnpm      |                                 | 全局安装pnpm                                |
| pnpm config get registry | https://registry.npmmirror.com/ | pnpm默认使用npm配置的源地址，一般不需要修改 |

