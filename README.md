# DeskSend

![DeskSend](desksend.png)

DeskSend 整合 Windows 键鼠共享和局域网文件传输。将文件拖过屏幕边缘，在副机松开鼠标后自动发送。

[下载最新完整包](https://github.com/wtyLaziness/desksend-releases/releases/latest)

解压完整目录后运行 **DeskSend.exe**，两台电脑均使用同版本的完整包，无需单独安装 LocalSend。请勿只复制一个 exe。

“帮助 → 检查 DeskSend 更新”可以检查正式版本、下载完整更新包、校验 SHA-256 并安装重启。便携版更新保留原有配置、证书和配对；安装前会备份待覆盖文件。

从旧版迁移时，先退出旧程序，再将旧目录的整个 `settings` 目录复制到新目录，覆盖新包的默认 `settings`，然后运行 DeskSend.exe。请保管好其中的私钥，不要公开上传。

默认键鼠连接使用 TCP 24800，副机的文件接收组件使用 TCP 53318。需要在 Windows 防火墙允许对应程序与端口。便携版不包含系统服务，不能控制 UAC 提示与登录界面。文件传输目前为主机到副机单向，空文件夹不传输。

## 源码与许可证

本仓库仅用于公开版本和更新渠道。每个 Release 均附带完整二进制包、对应版本的构建源码 zip 和 SHA256SUMS.txt；构建提交与逐文件哈希记录在包内 `desksend-build.json` 中。源码包包含修改后的 Deskflow、LocalSend 与构建脚本，不包含开发者本机配置、证书、日志和 Git 历史。

DeskSend 基于 [Deskflow](https://github.com/deskflow/deskflow)（GPL-2.0-only WITH OpenSSL exception）与 [LocalSend](https://github.com/localsend/localsend)（MIT），保留原作者版权与许可文件。图标融合两者的圆环和波纹形象。
