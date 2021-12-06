### get healthy instances ip 
```
aws elb describe-instance-health --region ap-southeast-1 --load-balancer-name prd-food-pax-api --output table --query  'InstanceStates[?State==`InService`].InstanceId'  | grep "i-" | awk '{print $2}' ORS=' '| xargs aws ec2 describe-instances --output json --query  'Reservations[*].Instances[*].PrivateIpAddress'  --instance-ids | grep "10.0" | awk -F '"'  '{print $2}'
```
