# Github connection

This template will create a github connection and export its ARN for use in different pipelines.  
Its is a create once and forget type of resource, use the export in all future pipelines and code builds.  
The connector require you to install the Github app "AWS Connector for GitHub" in github account or organization.  


## Create 

```
aws cloudformation create-stack --stack-name github-connection --template-body file://$PWD/cloudformation/github-connection.yml --profile pipelines
```


## Approve connection

In order to use the connection it need to be approved manually.
Login to your github service account, Avoid personal accounts as they will stop working when the user is removed from the organization.

* Find your connection in link and click it. https://eu-north-1.console.aws.amazon.com/codesuite/settings/connections
* Click "Finish creating your connection".  
* Put focus in the input field and wait for the autocomplete to show up.
* Select the github account and press "connect".

## Usage
In any cloudformation template. use Fn:ImportValue to fetch the connection ARN.
```
Fn::ImportValue: github-connection-CodeStarConnection
```