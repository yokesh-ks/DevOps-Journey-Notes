

AWS CLI Download: https://aws.amazon.com/cli/

AWS CLI Command Reference: https://awscli.amazonaws.com/v2/documentation/api/latest/reference/index.html

AWS Cloud Formation Templates Examples: https://github.com/awslabs/aws-cloudformation-templates

AWS Python Boto3 Example: https://gist.github.com/mda590/679aba60ca03699d5b12a32314debdc0

---

## AWS CLI

### 1. Amazon EC2 key pairs

https://docs.aws.amazon.com/cli/latest/userguide/cli-services-ec2-keypairs.html

To create 

```
aws ec2 create-key-pair --key-name MyKeyPair --query 'KeyMaterial' --output text > MyKeyPair.pem
```

To Display 

```
aws ec2 describe-key-pairs
```

Delete your key pair

```
aws ec2 delete-key-pair --key-name MyKeyPair
```

### 2. security groups for Amazon EC2

https://docs.aws.amazon.com/cli/latest/userguide/cli-services-ec2-sg.html

to dispaly vpc

```
aws ec2 describe-vpcs
```

To Create 

```
aws ec2 create-security-group --group-name my-sg --description "My security group" --vpc-id vpc-1a2b3c4d
```

To Display 

```
aws ec2 describe-security-groups
```

to authorize-security-group-ingress

```
aws ec2 authorize-security-group-ingress \
    --group-id sg-1234567890abcdef0 \
    --protocol tcp \
    --port 22 \
    --cidr 203.0.113.0/24
```

to Get Ip address - https://checkip.amazonaws.com/

### 3. Launching, listing, and terminating Amazon EC2 instances

https://docs.aws.amazon.com/cli/latest/userguide/cli-services-ec2-instances.html

```
aws ec2 run-instances --image-id ami-xxxxxxxx --count 1 --instance-type t2.micro --key-name MyKeyPair --security-group-ids sg-903004f8 --subnet-id subnet-6e7f829e
```


ami id - ami-01a4f99c4ac11b03c
keyName - Mytest111
group id - sg-0805ab2f834db79be

subnetid - subnet-09b64cc0a3033c97c


aws ec2 run-instances --image-id ami-01a4f99c4ac11b03c --count 1 --instance-type t2.micro --key-name Mytest111 --security-group-ids sg-0805ab2f834db79be --subnet-id subnet-09b64cc0a3033c97c
