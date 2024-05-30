**### Windows 使用命令行方法，实现 docker 默认安装目录修改及更改 docker 镜像默认保存路径**
**一、使用软连接方法，修改 Docker 默认安装目录**
查看 Windows 上安装 Docker Desktop 官方安装指南：
[https://docs.docker.com/desktop/install/windows-install/](https://docs.docker.com/desktop/install/windows-install/)
1、提前在 D 盘新建 Program\Docker，使用这行代码安装：
`"Docker Desktop Installer.exe"  install --installation-dir="PATH"`
2、" " 里面为你的 Docker Desktop Installer.exe 文件存放目录，PATH 替换你想要安装路径：
`"D:\Docker Desktop Installer.exe"  install --installation-dir="D:\Program\Docker"`
3、最后显示 Installation succeeded 代表安装成功。

**二、更改镜像默认保存路径**
1、运行 docker，进入设置页，点击 Resources 选项，发现镜像默认安装在 %UserProfile%\AppData\Local\Docker\wsl 目录下
2、点击 Browse 按钮，选择自定义的其他盘路径，例如：D:\Program\
3、最后点击 Apply & restart 按钮重启 Docker 即可生效。
4、docker 会自动在选定的目录下增加子目录 DockerDesktopWSL。