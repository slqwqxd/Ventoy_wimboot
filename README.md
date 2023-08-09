# 如何生成 ？
将本repo下载或克隆到桌面
## 在Wimdows下
1.安装Cygwin(https://cygwin.com/install.html)并安装mkisofs

2.提取Windows安装镜像中的bootmgr文件以及boot和efi文件夹到wimiso文件夹

3.为efi创建img 
```
(bash) mkisofs -o efi.img -J -R /cygdrive/c/users/你的用户名/desktop/wimiso-master/wimiso/efi/boot
```
你会在%desktop%/wimiso-master/wimiso/efi/下看到efi.img，请删除此目录下的boot文件夹
4.生成
```
(bash) mkisofs -no-emul-boot -boot-load-size 8 -b boot/etfsboot.com -o ventoy_wimboot.img -J -R /cygdrive/c/users/你的用户名/desktop/wimiso-master/wimiso
```
