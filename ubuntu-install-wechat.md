```shell
mkdir ~/git
cd ~/git
git clone https://gitee.com/wszqkzqk/deepin-wine-for-ubuntu.git
cd deepin-wine-for-ubuntu
./install.sh
```

```
wget https://gitee.com/wszqkzqk/deepin-wine-containers-for-ubuntu/raw/master/deepin.com.wechat_2.6.8.65deepin0_i386.deb
sudo dpkg -i deepin.com.wechat_2.6.8.65deepin0_i386.deb
```
1. 修改 run.sh 和 run_v2.sh 文件(操作都是一样的)
   这两个文件默认应该是在/opt/deepinwine/tools路径下
   修改 WINE_CMD，并添加三个 export 语句，内容如下

```shell
#WINE_CMD="deepin-wine"
WINE_CMD="LC_ALL=zh_CN.UTF-8 deepin-wine"

#added by user
export GTK_IM_MODULE="ibus"
export QT_IM_MODULE="ibus" 
export XMODIFIERS="@im=ibus"
```

```
cp msyh.ttc ~/.deepinwine/Deepin-WeChat/drive_c/windows/Fonts
gedit ~/.deepinwine/Deepin-WeChat/system.reg
"MS Shell Dlg"="msyh"
"MS Shell Dlg 2"="msyh"
```

## 字体注册

deepin-wine regedit msyh_config.reg

```
REGEDIT4
[HKEY_LOCAL_MACHINE\Software\Microsoft\Windows NT\CurrentVersion\FontLink\SystemLink]
"Lucida Sans Unicode"="msyh.ttc"
"Microsoft Sans Serif"="msyh.ttc"
"MS Sans Serif"="msyh.ttc"
"Tahoma"="msyh.ttc"
"Tahoma Bold"="msyhbd.ttc"
"msyh"="msyh.ttc"
"Arial"="msyh.ttc"
"Arial Black"="msyh.ttc"
```

