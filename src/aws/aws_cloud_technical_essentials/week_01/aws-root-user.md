# AWS Root User

- Keep in mind, the root user has complete access to all AWS Services and resources in your account, as well as your billing and personal information.

## Recomendations:

- Enable MFA - (Multi-Factor Authentication)
  - MFA can also be used to control access to specific AWS Services API
- Do not use root user for daily tasks.

## About Authentication

- Authentication ensures that the user is who they say they are. Usernames and password are the most common types of authentication. However you may also work with other forms , such as token-based authentication or biometric data like a fingerprint. Authentication simply answers the question, "Are you who say you are?"

## About Authroization

- It is the process of giving users permission to access AWS resources and services. This determines whether the user can perform an action, like read, edit, delete, or create resources. Authorization answers the question, "What actions can you perform?"

## Understanding the AWS Root User Credentials

- The AWS root users has two sets of credentials associated with it.
  - Firstly, is the email and password used to create the accound.
  - Secondly, is called access key, which allow you to make programmatic requests from the AWS CLI or AWS API.
    - An access keys consists of two part:
      - An access key ID.
      - An secret access key.
    - Access Key should be managed with the same security as an email address and password.

## Best Practices when working with the AWS Root User

- To ensure the safety if the root user:
  - Choose a strong password.
  - Never share your root password or access keys with anyone.
  - Disable or delete the access keys associated with the root user.
  - Do not use the root user for administrative tasks or everyday tasks.
  - Enable MFA.

## Resources

- [Enabling a Hardware MFS Device (Console)](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_mfa_enable_physical.html)
- [Enabling a U2F Security Key (Console)](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_mfa_enable_fido.html)
- [Enabling a Virtual Multi-Factor Auhtentication (MFA) Device (Console)](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_mfa_enable_virtual.html)
- [Table of Supported MFA Devices](https://aws.amazon.com/iam/features/mfa/)
- [Tasks that require the use of root user credentials](https://docs.aws.amazon.com/IAM/latest/UserGuide/security-creds.html#aws_tasks-that-require-root)
