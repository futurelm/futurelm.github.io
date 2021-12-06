### run commands on every work node 
1. get all node ip 
  ```
  kc get node -o wide |grep Ready |awk '{print $6}' ORS=','
  ```
2. run ansible 
```
ansible -i 10.197.164.153,10.197.164.28,10.197.165.138,10.197.165.167,10.197.166.70,10.197.166.82,10.197.167.249 --key-file ~/.ssh/id_rsa -m sudo docker system 
```
