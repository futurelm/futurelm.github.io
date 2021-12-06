### run commands on every work node 
1. get all node ip 
  ```
  kc get node -o wide |grep Ready |awk '{print $6}' ORS=','
  ```
2. run ansible on hosts
```
ansible all -i "10.197.164.153,10.197.164.28," --key-file ~/.ssh/id_rsa -u ec2-user -a "df -h" 
```
