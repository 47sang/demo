[安装后更新](#%E5%AE%89%E8%A3%85%E5%90%8E%E6%9B%B4%E6%96%B0)

- [安装后更新](#%E5%AE%89%E8%A3%85%E5%90%8E%E6%9B%B4%E6%96%B0)
- [install 搜狗输入法](#install-%E6%90%9C%E7%8B%97%E8%BE%93%E5%85%A5%E6%B3%95)
- [git setting](#git-setting)
- [启动项修改](#%E5%90%AF%E5%8A%A8%E9%A1%B9%E4%BF%AE%E6%94%B9)
- [安装 chrome](#%E5%AE%89%E8%A3%85-chrome)
  - [设置成默认浏览器；](#%E8%AE%BE%E7%BD%AE%E6%88%90%E9%BB%98%E8%AE%A4%E6%B5%8F%E8%A7%88%E5%99%A8)
- [更换终端](#%E6%9B%B4%E6%8D%A2%E7%BB%88%E7%AB%AF)
- [安装 vs code](#%E5%AE%89%E8%A3%85-vs-code)
- [ubuntu KVM 问题](#ubuntu-kvm-%E9%97%AE%E9%A2%98)

# 安装后更新

- sudo apt update
- sudo apt upgrade

# install 搜狗输入法

- 下载软件包https://pinyin.sogou.com/linux/

- sudo apt install ./{feilname}.deb

- sudo apt install ./sogoupinyin_2.2.0.0108_amd64.deb

# git setting

- git config --global user.email "zhoushiyu92@gmail.com"
- git config --global user.name "47sang"

# 启动项修改

- sudo gedit /etc/default/grub

- 上面的命令找不到就用：vi 打开文件；

- sudo update-grub

- 然后后更新；

# 安装 chrome

- 添加软件源

- sudo wget http://www.linuxidc.com/files/repo/google-chrome.list -P /etc/apt/sources.list.d/

- wget -q -O - https://dl.google.com/linux/linux_signing_key.pub | sudo apt-key add -

- sudo apt-get update

- sudo apt-get install google-chrome-stable

- /usr/bin/google-chrome-stable

## 设置成默认浏览器；

- sudo update-alternatives --config x-www-browser

# 更换终端

- sudo apt-get install git

- sudo apt-get install zsh

- wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | sh

- chsh -s /usr/bin/zsh

# 安装 vs code

- https://code.visualstudio.com/

# ubuntu KVM 问题

- 查看用户权限和归属，授权，更改授权
- ls -al /dev/kvm
- sudo chmod -R 755 /dev/kvm
- sudo chown <你系统当前的登陆用户名> -R /dev/kvm
-
