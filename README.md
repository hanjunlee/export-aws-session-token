# AWS token controller

## Why export-aws-session-token?

AWS  is supporting cli MFA by session token. The command is `aws sts get-session-token --serial-number arn:aws:iam::USER-ID:mfa/USER-NAME --token-code XXXXXX`, and the output skeleton is like below. But it is bothering to copy keys, there is needs to do this boring stuff automatically.

```
{
    "Credentials": {
        "SecretAccessKey": "XXXXXXXXXXXXXXXXXXXXXXXXXXXX",
        "SessionToken": "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX",
        "Expiration": "2019-01-06T04:58:13Z",
        "AccessKeyId": "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
    }
}
``` 

## Installation

Check the [releases](./releases) for the latest version.

### Linux

Here's how it could look for 64 bits Linux, if you wanted tffilter available globally inside /usr/local/bin:

```
curl -SsL https://github.com/hanjunlee/awsprofile/releases/download/v0.1/awsprofile.v0.1_linux_amd64 \
  | sudo tee /usr/local/bin/export-aws-session-token > /dev/null && sudo chmod 755 /usr/local/bin/export-aws-session-token
```

### OSX

Here's how it could look for 64 bits Darwin, if you wanted tffilter available globally inside /usr/local/bin:

```
curl -SsL https://github.com/hanjunlee/awsprofile/releases/download/v0.1/awsprofile.v0.1_darwin_amd64 \
  | sudo tee /usr/local/bin/export-aws-session-token > /dev/null && sudo chmod 755 /usr/local/bin/export-aws-session-token
```

## Version
 
### version 0.1

Initialize `aws-session-token` command.
