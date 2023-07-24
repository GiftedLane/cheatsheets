AWS CLI Commands
===============

Create SSM parameters using the AWS CLI 
----
_# Sample AWS SSM parameter JSON file_
```json
{
    "Parameters": [
        {
            "Name": "/myapp/database/username",
            "Type": "SecureString",
            "Value": "mydbusername",
            "KeyId": "alias/myapp/dbkey"
        },
        {
            "Name": "/myapp/database/password",
            "Type": "SecureString",
            "Value": "mydbpassword",
            "KeyId": "alias/myapp/dbkey"
        },
        {
            "Name": "/myapp/api-key",
            "Type": "String",
            "Value": "myapikey"
        }
    ]
}

```
```shell
# sample of command needed
aws ssm put-parameter --name "my-parameter-name" --type "SecureString" --value "my-parameter-value" --key-id "my-kms-key-id"
```
_# spit out the `aws ssm put-parameter` command (with Key IDs) to a txt file_
```swift
cat ssm-params.json | jq -r '.Parameters[] | "aws ssm put-parameter --name \"" + .Name + "\" --type \"" + .Type + "\" --value \"" + .Value + "\"\(.KeyId | select(. != null) | " --key-id \"" + . + "\"")"' > someFileName.txt
```
_# spit out the `aws ssm put-parameter` command (withOUT Key IDs) in terminal_
```swift
cat ssm-params.json | jq -r '.Parameters[] | "aws ssm put-parameter --name \"" + .Name + "\" --type \"" + .Type + "\" --value \"" + .Value + "\"\(.KeyId | select(. == null) | " --key-id \"" + . + "\"")"'
```
```shell
# navigate to AWS config location
cd ~/.aws
```
