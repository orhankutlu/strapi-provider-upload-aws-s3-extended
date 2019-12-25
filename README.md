# strapi-provider-upload-aws-s3-extended

## Resources

- [MIT License](LICENSE.md)

## Description

This package extends strapi's aws-s3-upload provider. The key differences are

1. Reads the AWS credentials from the environment variables.
2. Allows admins to select default ACL's for the uploads.

## Set AWS Credentials
You need to add a new property called `aws` to your `custom.json` file(s) and set your credentials as follows.

```
// environments/*/custom.json
{
  "customConfig": "This configuration is accessible through strapi.config.environments.development.myCustomConfiguration",
  "aws": {
    "accessKeyId": "${process.env.AWS_ACCESS_KEY_ID} || AWS Access Key Id",
    "secretAccessKey": "${process.env.AWS_SECRET_ACCESS_KEY} || AWS Secret Key"
  }
}
```
You can rename the `environment variables` as you like.