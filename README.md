# What is it?
It's a simple shell script that is used by me to enable easy access to other AWS accounts using STS and cross account roles.

# Why would I need it?
It is convenient in the following cases:
  
  * Your application is not compatible with boto profiles (like **Ansible**)
  * Your cross account role requires MFA tokens
  * For some other reasons you need pure AWS keys instead of boto profile

# How can I use it?

Just set variables at the beginning of the script (don't have time to make it more fancy). After you launch it you can source shell script that it generates (it will also delete itself for your security).

Enjoy!
