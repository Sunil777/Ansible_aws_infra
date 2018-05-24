# Overview: Ansible_aws_infra


BCP is a necessary approach for all organization. Before using this playbook kindly check Snapshot process of EC2 [SNAPSHOT](https://github.com/Sunil777/AWS_EC2_SNAPSHOT/).
- - - -
# Usage

```
boto version :-  boto3
Jinja2 version :- Jinja2
```

Ansible version

        >= 2.2.0.0

How we can execute this playbook

        ansible-playbook main.yml --extra-vars 'host=localhost INCREMENTAL=daily PORT=$SSH_PORT ec2_assign_public_ip=no  USER=$USER  PASSWD=******** ec2_count=1 ec2_sg_id=$SG_ID   elb_name=$ELB_NAME  ec2_monitoring=yes subnet1=$1 subnet2=$2  stack=$STACK region=ap-south-1 ec2_key_name=$KEY_NAME ec2_instance_type=c5.large server=$STACK env=prod expday=3'



I hope you can see where this is going.

- - - -
# References

1. [Master Ansible](https://books.google.com/books?id=bvSoCwAAQBAJ&pg=PA67&lpg=PA67&dq=ansible+nested+filters&source=bl&ots=Nfj9uX6i84&sig=eLmypWMp8ZVLbKkZVFJbZtdDi8w&hl=en&sa=X&ved=0ahUKEwjuhdKmpMrQAhVs5IMKHdhCDa44FBDoAQgaMAA#v=onepage&q=ansible%20nested%20filters&f=false)
1. [Ansible documentation on filters](http://docs.ansible.com/ansible/playbooks_filters.html)
