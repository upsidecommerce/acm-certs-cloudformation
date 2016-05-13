This is a fork of [ryansb/acm-certs-cloudformation](https://github.com/ryansb/acm-certs-cloudformation), which adds custom AWS Lambdas
for creating and associating AWS ACM resources with Cloudfront Distributions (A feature currently lacking in CF).

This fork fixes a simple error-handling bug as well as allows for the setting of ACM region, which is necessary
in order to associate an ACM certificate to resources outside of us-east-1 (the only supported region of ACM)

To publish changes:
```
make clean
make acm-functions.zip
```

once acm-function.zip if build, upload it to S3 (s3://cloudformation-086114645662/custom-functions/acm-functions.zip)
