# What is it?
It's a improved version of simple shell script forked from cloudowski that is used by me to enable easy access to other AWS accounts using STS and cross account roles as well as MFA

# Why would I need it?
It is convenient in the following cases:

  * Your application is not compatible with boto profiles (like **Ansible**)
  * Your cross account role requires MFA tokens
  * To support Terraform s3-dynamodb state backends

# How can I use it?

Set the variables in 3 sourced files
* ~/.aws/mfa to set MFA device ARN and OTPKEY Name
* ~/.aws/cross-account-roles to set destination role ARN and optionally AWS config profile
* ~/.otpkeys - to provide OTPKEY name with corresponding OTP Key

e. g.

To switch to development account just use argument which is mapped in .aws/cross-account-roles file
```
./aws-crossaccount-keys dev

```

New aws keys are set as a default profile in ~/.aws/credential ~/.aws/config
Previous default profile is renamed as [main], so you can still use it, by explicitly reference to [main]

**Many thanks for Cloudowski who provided the first version!**
**Enjoy!**
