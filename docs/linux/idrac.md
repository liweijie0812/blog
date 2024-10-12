# iDRAC
## 通过ssh 打隧道访问 idrac 400 错误
[方案来源](https://www.dell.com/support/kbdoc/en-in/000193619/http-https-fqdn-connection-failures-on-idrac9-firmware-version-5-10-00-00?dgc=SM&cid=376139&lid=spr8799951350&refid=sm_LITHIUM_spr8799951350&linkId=199564916)

ssh 进入 idrac 修改 HostHeaderCheck 为 0
```sh
racadm>> set idrac.webserver.HostHeaderCheck 0
```
查询 HostHeaderCheck 状态
```sh
racadm>> get idrac.webserver.HostHeaderCheck
```