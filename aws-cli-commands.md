<div style="background-color: #f9f9f9; border-left: 6px solid #3f51b5; padding: 0.5em;">
  🎮 <strong>The Legend of Zelda: Tears of the Kingdom</strong>: <em>was played heavily between completing Terraform labs.</em>
</div>

### Table of Contents

- [Install AWS CLI](#install)
- [Help Command](#help-command)
- [Configure AWS CLI](#configure-aws-cli)
- [View Commands](#view-commands)
- [IAM Commands](#iam-commands)
- [SSM Parameters](#ssm-parameters)
- [Resources](#resources)

# AWS CLI Commands

### Install

```shell
#install aws cli using the bundled installer:
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o awscli-exe-linux-x86_64.zip
unzip awscli-exe-linux-x86_64.zip
sudo ./awscli-bundle/install -i /usr/local/aws -b /usr/local/bin
```

```bash
# Using pip:
sudo pip3 install awscli
```

### Help Command

```shell
#iam help
aws iam help
```

### Configure AWS CLI

```bash
#configure aws cli
aws configure
```

```bash
#navigate to config file
cd ~/.aws
```

### View Commands

```bash
#view AWS CLI version
aws --version
```

```bash
#list all IAM Users
aws iam list-users

#using the endpoint option
aws --endpoint http://aws:4566 iam list-users
```

### IAM Commands

```bash
#create new user
aws iam create-user --user-name mipha
```

### SSM Parameters

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


### Resources

- [AWS CLI Getting Started Guide](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-quickstart.html)
- [AWS CLI Command Reference](https://docs.aws.amazon.com/cli/latest/index.html)

---
