# Wordpress server stack.

Create stack with this command from this folder:
```
aws cloudformation create-stack --stack-name your-stack-name --template-body file://$PWD/cloudformation/stack.yml --parameters ParameterKey=DeployPublicKey,ParameterValue="{deploy user public key}" ParameterKey=GithubAccount,ParameterValue="{this github account}" ParameterKey=GithubRepo,ParameterValue="{this github repo}" ParameterKey=VPCID,ParameterValue="{vpc id}"
```

## Required Parameters
Add to create command as such `ParameterKey=ParameterName,ParameterValue="Value"`

- GithubRepo 
- GithubAccount 
- DeployPublicKey 
- VPCID
- InstanceName

## Optional Parameters
Add to create command as such `ParameterKey=ParameterName,ParameterValue="Value"`

- InstanceType 
- VolumeSize 
- EC2KeyName 
