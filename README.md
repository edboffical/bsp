**bsp是shadowsocks多用户、流量、限时管理接口 - 微博:str8** 

---

支持shadowsocks-python和shadowsocks-Go

 **安装** 

```
git clone https://github.com/edboffical/bsp.git
cd bsp
chmod 775 install
./install
```

对于其他地方下载的shadowsocks，修改部分文件后也可使用。比如，我前段时间使用下列下载的shadowsocks：
```
wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks.sh 
```

**修改**

将`bsp/byte_ss.json`文件中的下列两行，
```
"ssconf_path":"/etc/shadowsocks-python/config.json",
"ress_cmd":"/etc/init.d/shadowsocks-python restart", 
```
修改为：
```
"ssconf_path":"/etc/shadowsocks.json",
"ress_cmd":"/etc/init.d/shadowsocks restart",
```

详细使用请查阅使用文档 [wiki](https://github.com/edboffical/bsp/wiki/bsp%E7%9A%84%E5%AE%89%E8%A3%85%E4%BD%BF%E7%94%A8)

利用web分支搭建多节点、限时流量管理系统(一般的商用架构)参阅 [wiki](https://github.com/edboffical/bsp/wiki/%E4%BD%BF%E7%94%A8bsp%E6%90%AD%E5%BB%BA%E5%A4%9A%E8%8A%82%E7%82%B9%E3%80%81%E9%99%90%E6%97%B6%E6%B5%81%E9%87%8F%E7%AE%A1%E7%90%86%E7%B3%BB%E7%BB%9F)
