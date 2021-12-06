### ORS， 合并多行输出到一行，并分割
example 
```
➜ ls
food-max-email-logging.yaml      latest.log                       multi-containers.yaml            new-food-max-email.yaml          rsyslog-conf-food-max-email.yaml sre.yaml                         temp.yaml
```
resutlt
```
➜ ls | grep 'yaml'|awk '{print $1}' ORS=','
food-max-email-logging.yaml,multi-containers.yaml,new-food-max-email.yaml,rsyslog-conf-food-max-email.yaml,sre.yaml,temp.yaml,
``` 
