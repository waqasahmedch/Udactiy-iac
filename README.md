# Udactiy-iac
Deploy a high-availability web app using AWS CloudFormation


Sequence of deloyment 

aws cloudformation create-stack --stack-name UdagramNetwork --template-body file://Udagram-Network-v2.yml  --parameters file://Udagram-Network-v2.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=us-east-1

aws cloudformation create-stack --stack-name UdagramInfra --template-body file://Udagram-Infra-v2.yml  --parameters file://Udagram-Infra.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=us-east-1


-- Optional , if you wish to troubleshoot your Instances, you may create a Jump host and login to instances in private subnets. But i requires some changes like KeyPairs for security reasons. You may also required to add KeyPairs names in Udagram-Infra-v2.yml file in section or line 66 (add new Line) and write KeyName: <your key name>
aws cloudformation create-stack --stack-name UdagramBastian --template-body file://Udagram-Bastian.yml  --parameters file://Udagram-Bastian.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=us-east-1
