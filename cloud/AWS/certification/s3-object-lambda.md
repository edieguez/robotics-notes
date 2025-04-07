# S3 Object Lambda

Is a feature of **S3** that allows you to add your own code to S3 GET requests to modify and process data as it is returned to an application. It allows you to use AWS Lambda functions to modify the data returned by an S3 GET request. This feature is useful when you want to transform data as it is being read from an S3 object

Only one S3 bucket is needed on top of which we create S3 Access Point and S3 Object Lambda Access Points

## Use cases

- Redacting personally identifiable information for analytics or non-production environments
- Converting across data formats, such as converting XML to JSON
- Resizing and watermarking images on the fly using caller-specific details, such as the user who requested the object
