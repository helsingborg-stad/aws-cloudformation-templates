# ToMoveItPOC DynamoDB

Create stack.
```
aws cloudformation create-stack --stack-name tomoveit-poc-dynamodb --template-body file://$PWD/cloudformation/stack.yml --capabilities CAPABILITY_IAM
```

Update stack.
```
aws cloudformation update-stack --stack-name tomoveit-poc-dynamodb --template-body file://$PWD/cloudformation/stack.yml --capabilities CAPABILITY_IAM
```

Delete stack.
```
aws cloudformation delete-stack --stack-name tomoveit-poc-dynamodb 
```