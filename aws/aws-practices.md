# AWS Practices

When requesting spot instances, request instances of various types so that if the bid price changes and you lose instances you dont lose all of them at once.


The best way to create login profiles is described in the aws docs:

http://docs.aws.amazon.com/cli/latest/reference/iam/create-login-profile.html

Using the --cli-input-json option avoids saving a password to your commandline history and handles weird characters.
