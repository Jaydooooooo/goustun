#项目地址
https://github.com/go-gost/gost
#下载二进制文件

#解压
tar -xzf gost_3.0.0-nightly.20240426_linux_amd64.tar.gz -C /usr/local/bin

#赋权
chmod +x /usr/local/bin/gost

#运行
gost -h

#github一键安装

bash <(curl -fsSL https://github.com/go-gost/gost/raw/master/install.sh) --install

#中转鸡命令1
nohup gost -L tcp://:中转机入站端口 -F relay+wss://中转机IP:中转机出站端口 &

#中转鸡命令2
nohup gost -L relay+wss://:中转机出站端口/落地机IP:落地机端口 &  #这里默认中转机的出站端口和落地机的出站端口一样

#查看进程
ps aux | grep gost

