# DEMO_LAN

## 3.1 Настройка деномической трансляции адресов 
### на isp:
nano /etc/nftables/isp.nft

### прописываем: 
table inet nat {
        chain POSTROUTING {
        type nat hook postrouting priority srcnat;
        oifname "enp0s3" masquerade
        }
}
