# 内蒙古师范大学附属中学 in Minecraft 项目服务端

## 项目简介

该项目是一个计划在 MC 中 1:1 搭建还原内蒙古师范大学附属中学的项目，早期为私人服务器，由 `Frspble、Keerqinfu、starchen` 三人参与建造。后由 Frspble 于 2023 年 1 月 15 日将服务器迁移到公网，并在 B 站发布视频进行宣传，得到了许多志同道合的校友的支持，`jokershiisme、Hazukimio、R3medy、star_dust__、aaady、lqndwyy、lzl66、hangez、QGeq、WRQ` 等人陆续加入服务器参与建造。服务器原计划运行一个月，之又后在`hangez`的赞助下，服务器又续费一年。最终于 2024 年 2 月 14 日到期关闭并开源，欢迎有兴趣的校友将服务器继续建设下去。

**如果你计划使用该项目中的游戏存档，请遵循类似 GPL 的协议：**

1. **存档的内容可以随意修改，但修改后必须将新存档开源，且必须包含该协议。**
2. **在新存档中必须保留原有的贡献者信息。**
3. **游戏存档中的任何内容均不得用于商业用途。**
4. **如要建立服务器，针对校友不得设置任何的进入门槛。**

## 服务器搭建指南

服务器搭建时可以选用云服务器，也可以自建服务器。对操作系统没有要求，只需保证系统中 Java 版本大于 17，并且内存在 4GB 以上（内存越大支持的同时在线人数越多）。如果在云服务器上搭建服务器，建议使用 MCSＭ 面板，可以很方便的管理服务器。

服务器的软件环境准备好后，可以直接在命令行中输入服务器启动命令：

```bash
java -javaagent:authlib-injector-1.2.1.jar=https://wzs.minecraftlogin.org/api/yggdrasil -jar paper-1.19.2-307.jar
```

该启动指令中包含了我们[自建验证皮肤站](https://wzs.minecraftlogin.org)服务器的地址，各位在建立服务器时可以使用我们的皮肤站，也可以自建皮肤站，但不得对校友设置任何的进入门槛。

## 关键目录和文件说明

该服务器在搭建时使用 Paper 服务端搭建，Minecraft 版本为 1.19.2，并且选用了对应版本的服务器插件。如需修改服务端请注意游戏版本兼容。下面是一些关键目录的说明：

```
├── config                         # Paper 服务器设置
│   ├── paper-global.yml
│   ├── paper-world-defaults.yml
├── plugins                        # 插件目录
│   ├── Essentials                 # 服务器功能增强插件
│   ├── GroupManager               # 用户权限管理插件
│   ├── Law                        # 规则增强插件（主要用于限制爆炸和生物生成）
│   └── WorldEdit                  # 创世神插件
├── world                          # 地图存档
│
├── authlib-injector-1.2.1.jar     # 验证服务器 jar 包
├── paper-1.19.2-307               # paper 服务端 jar 包
├── README.md                      # 项目说明文件
├── server.properties              # 服务器配置文件

```
