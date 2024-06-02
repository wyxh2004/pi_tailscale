<img alt="GitHub License" src="https://img.shields.io/github/license/wukongdaily/diy-nas-onescript?labelColor=%23FF4500&color=black"> 

本项目基于 https://github.com/wukongdaily/OrangePiShell 修改，主要变动为使用**tailscale**实现内网穿透，同时进行了一些删改

### 适用于 `Ubuntu` / `Debian` / `Synology` 等基于 Debian 的 Linux 脚本
```bash
wget -qO pi.sh https://cafe.cpolar.cn/wkdaily/zero3/raw/branch/main/zero3/pi.sh && chmod +x pi.sh && ./pi.sh
```

<!-- ### OpenWrt / iStoreOS 软路由系统

```bash
wget -qO op.sh https://cafe.cpolar.cn/wkdaily/zero3/raw/branch/main/zero3/op.sh && chmod +x op.sh && ./op.sh
``` -->

<!-- <img src="https://cafe.cpolar.cn/wkdaily/zero3/releases/download/v1/pre.jpg" width="40%" /> -->

### 链接
- **Tailscale 官网**: https://tailscale.com/
- **FielBrowser 官网**: https://filebrowser.org/
- **1Panel 官网**: https://1panel.cn/
- **docker 离线包**：https://drive.google.com/drive/folders/1DrjTXzLKUvhQzd79kMvY0j5nGqdCNVIu

# 兼容的系统（ARM64 / AMD64）

| 系统 | 或 |机型  |
|-----|-----|-----|
| Ubuntu ✅ | Debian ✅ | Deepin ✅ |
| OpenWrt ✅ | iStoreOS ✅ | MT-3000 ✅ |
| NanoPi-R2S ✅ | NanoPi-R4S ✅ | NanoPi-Neo3 ✅ |
| Synology ✅ | QNAP ✅ |UNRAID ✅   |
| Raspberrypi ✅ | PVE ✅|Zero3 ✅  |

# 常见问题汇总⬇️⬇️⬇️

[filebrowser 如何设置自定义端口](https://github.com/wukongdaily/OrangePiShell/wiki/filebrowser-%E5%A6%82%E4%BD%95%E8%AE%BE%E7%BD%AE%E8%87%AA%E5%AE%9A%E4%B9%89%E7%AB%AF%E5%8F%A3)

[常见问题总结（持续更新中](https://github.com/wukongdaily/OrangePiShell/wiki/%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98)

[常见问题总结（持续更新中）](https://cafe.cpolar.cn/wkdaily/zero3/wiki/%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98%E6%B1%87%E6%80%BB)

# 如何定时重启小雅？
[使用1panel 添加定时任务即可](https://cafe.cpolar.cn/wkdaily/zero3/wiki/%E5%A6%82%E4%BD%95%E5%AE%9A%E6%97%B6%E9%87%8D%E5%90%AF%E5%B0%8F%E9%9B%85)

# 小雅 alsit 和 小雅 tvbox 有啥区别吗？
```
截止到我做视频的时候，小雅alist和小雅tvbox是有如下区别的。
1、小雅alist 是比较轻量化的docker。主要是影音库或者理解为一个云端的数据库。它占用内存较低，最多200M内存吧，
如果你的宿主机内存不大，那么我建议安装这个（视频里演示的那种）。而小雅tvbox，是针对tvbox 这款软件做了一些定制的，
貌似是用java写的后端？我也不确定，实际测试这款docker大约占用600M内存。x86和arm 都是如此。
```
```
2、小雅tvbox 集成了友好的WebUI管理页面，你可以很方便的在4567端口的web页，添加阿里、pikpak账号。
你还可以定制化tvbox的订阅，详细的文档建议参考作者的项目
https://github.com/power721/alist-tvbox/blob/master/doc/README_zh.md
（该作者写的文档相当的细致 爆赞👍）功能很多，配合tvbox 堪称完美！
```
```
3、小雅alist 搭建后，最好是配合安装小雅转存清理工具xiaoya-keeper，因为它每次播放或者用播放器搜刮的时候
可能会转存一份到自己的云盘。如果有这个清理工具就能帮助它迅速删除。避免占用自己的空间。而小雅tvbox 则不需要。
因为小雅tvbox默认900秒清理一次文件。不过这个数值可以更改为60秒。就在4567网页的高级配置里。
```
```
4、小雅alist 的影音数据库的更新操作依赖于容器的重启。因此最好设置一个定时任务，定时重启。（这只是目前为止，
或许以后作者会加入定时更新的功能，大家还是自行观察每天数据库到底有没有更新，以实际为准。）
而小雅tvbox，由于在4567的web页面 已经默认开启了定时更新功能，并且还能设置更新的时间。
```
```
5、小雅alist默认端口号5678，小雅tvbox默认端口号5344，这个端口号很重要，webdav如果写错了端口号是无法读取的。
```
```
6、小雅alist和小雅tvbox大家二选一就行。尽量别重复搭建。因为小雅tvbox搭建的时候应该也会拉取小雅alist
这样就重复了。
```


<img src="https://static.har01d.cn/tvbox/atv_bilibili.png" width="80%"/>

# 参考项目
- https://github.com/DDS-Derek/xiaoya-alist
- https://har01d.cn/#/notes/alist-tvbox
