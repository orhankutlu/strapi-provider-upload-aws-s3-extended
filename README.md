# strapi-provider-upload-aws-s3-ext

## Resources

- [MIT License](LICENSE.md)

## Install

`npm install strapi-provider-upload-aws-s3-ext` 

## Description

This package extends strapi's aws-s3-upload provider. The key differences are

1. Reads the AWS credentials from the environment variables.
2. Allows admins to select default ACL's for the uploads.

## Set AWS Credentials
You need to add a new property called `aws` to your `config/custom.json` file(s) and set your credentials as follows.

```
// config/custom.json
{
  "customConfig": "This configuration is accessible through strapi.config.environments.development.myCustomConfiguration",
  "aws": {
    "accessKeyId": "${process.env.AWS_ACCESS_KEY_ID || AWS Access Key Id}",
    "secretAccessKey": "${process.env.AWS_SECRET_ACCESS_KEY || AWS Secret Key}"
    "customBaseUrl": "${process.env.CDN_BASE_URL || 'https://cdn.example.com/'}"
  }
}
```
You can rename the `environment variables` as you like.
