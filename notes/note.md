# install 搜狗输入法

- 下载软件包https://pinyin.sogou.com/linux/
- sudo apt install ./{feilname}.deb
- sudo apt install ./sogoupinyin_2.2.0.0108_amd64.deb

# git setting

git config --global user.email "zhoushiyu92@gmail.com"
git config --global user.name "47sang"

# 启动项修改

sudo gedit /etc/default/grub

- 上面的命令找不到就用：vi 打开文件；
  sudo update-grub
- 然后后更新；

# 安装 chrome

- 添加软件源

sudo wget http://www.linuxidc.com/files/repo/google-chrome.list -P /etc/apt/sources.list.d/

wget -q -O - https://dl.google.com/linux/linux_signing_key.pub | sudo apt-key add -

sudo apt-get update

sudo apt-get install google-chrome-stable

/usr/bin/google-chrome-stable

- 设置成默认浏览器；

sudo update-alternatives --config x-www-browser
