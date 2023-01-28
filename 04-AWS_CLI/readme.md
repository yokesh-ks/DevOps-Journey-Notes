

AWS CLI Download: https://aws.amazon.com/cli/

AWS CLI Command Reference: https://awscli.amazonaws.com/v2/documentation/api/latest/reference/index.html

AWS Cloud Formation Templates Examples: https://github.com/awslabs/aws-cloudformation-templates

AWS Python Boto3 Example: https://gist.github.com/mda590/679aba60ca03699d5b12a32314debdc0




AWS CLI

1. Amazon EC2 key pairs

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

2. 
