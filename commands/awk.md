### ORS， combines multi outputs to one line 
```
➜ ls | grep 'yaml'|awk '{print $1}' ORS=','
food-max-email-logging.yaml,multi-containers.yaml,new-food-max-email.yaml,rsyslog-conf-food-max-email.yaml,sre.yaml,temp.yaml,
``` 
