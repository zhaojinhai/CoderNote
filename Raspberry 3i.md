# 树莓派3 B+学习笔记(Raspbian)
- ##  默认用户名及密码 
>用户名:pi 密码:raspberry
- ## 配置网络
>sudo vi /ect/nectwork/interfaces 
    
    auto eth0
    iface eth0 inet static
        #Ip地址
        address 192.168.1.36          
        network 192.168.1.0    
        #子网掩码
        netmast 255.255.255.0
        broadcast 192.168.0.255
        #网关
        gateway 192.168.1.254

- ## 配置Wifi
>sudo vi/ect/network/interfaces

    iface wlan0 inet dhcp
>sudo vi/etc/wpa_supplicant/wpa_supplicant.conf
     
    network={
        ssid="wifi的名子"
        psk="连接密码"
    }
>重启无线网卡  
sudo ifdown wlan0  
sudo ifup wlan0