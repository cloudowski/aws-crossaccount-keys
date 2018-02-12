# What is it?
It's a improved version of simple shell script forked from cloudowski that is used by me to enable easy access to other AWS accounts using STS and cross account roles as well as MFA

# Why would I need it?
It is convenient in the following cases:

  * Your application is not compatible with boto profiles (like **Ansible**)
  * Your cross account role requires MFA tokens
  * For some other reasons you need pure AWS keys instead of boto profile

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

New aws keys are automatically exported in a current shell

**Many thanks for Cloudowski who provided the first version!**
**Enjoy!**
