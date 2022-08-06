# Udactiy-iac
Deploy a high-availability web app using AWS CloudFormation


Sequence of deloyment 
aws cloudformation create-stack --stack-name UdagramNetwork --template-body file://Udagram-Network.yml  --parameters file://Udagram-Network.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=us-east-1

aws cloudformation create-stack --stack-name UdagramInfra --template-body file://Udagram-Infra.yml  --parameters file://Udagram-Infra.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=us-east-1

aws cloudformation create-stack --stack-name UdagramBastian --template-body file://Udagram-Bastian.yml  --parameters file://Udagram-Bastian.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=us-east-1

