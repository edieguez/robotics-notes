# S3 presigned URLs

## What is a presigned URL?

A presigned URL is a URL that you can provide to your users to grant temporary access to a specific S3 object. This URL can be used to perform actions on the object, such as downloading or uploading it, without requiring the user to have AWS credentials

> Users given a pre-signed URL inherit the permissions of the user that generated the URL for `GET/PUT`*

They can be generated using

- S3 console
- AWS CLI
- AWS SDKs

## URL expiration

- `S3 console` 1 minute up to 720 minutes (12 hours)
- `AWS CLI` 1 second up to 604800 seconds (168 hours or 7 days)

## Use cases

- Allow only logged-in users to download a premium video from your S3 bucket
- Allow an ever-changing list of users to download files by generating URLs dynamically
- Allow temporarily a user to upload a file to a precise location in your S3 bucket
- Share confidential data with a third party
