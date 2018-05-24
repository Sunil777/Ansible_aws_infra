# Overview: Ansible_aws_infra


BCP is a necessary approach for all organization. Before using this playbook kindly check have we can take snapshot of ec2 [SNAPSHOT](https://github.com/Sunil777/AWS_EC2_SNAPSHOT/)
- - - -
# Usage

```
boto version :-  boto3
Jinja2 version :- Jinja2
```

Ansible version

        >= 2.2.0.0

Match a set of tags exactly and get the returned instance(s)

        ansible-playbook playbook.yml -e cli_env=prod -e cli_roles=app,web,db

Glob all boxes with role of `web` somewhere in the list and get the returned instance(s). This is where this method gets weird and you can potentially match too many boxes. **Be careful**. Always run with --list-hosts first.

        ansible-playbook playbook.yml -e cli_env=prod -e cli_roles=*web* --list-hosts
        ansible-playbook playbook.yml -e cli_env=prod -e cli_roles=*web*

Glob all boxes with role of `jenkins*` and get the returned instance(s)

        ansible-playbook playbook.yml -e cli_env=prod -e cli_role=jenkins*

I hope you can see where this is going.

- - - -
# References

1. [Master Ansible](https://books.google.com/books?id=bvSoCwAAQBAJ&pg=PA67&lpg=PA67&dq=ansible+nested+filters&source=bl&ots=Nfj9uX6i84&sig=eLmypWMp8ZVLbKkZVFJbZtdDi8w&hl=en&sa=X&ved=0ahUKEwjuhdKmpMrQAhVs5IMKHdhCDa44FBDoAQgaMAA#v=onepage&q=ansible%20nested%20filters&f=false)
1. [Ansible documentation on filters](http://docs.ansible.com/ansible/playbooks_filters.html)
