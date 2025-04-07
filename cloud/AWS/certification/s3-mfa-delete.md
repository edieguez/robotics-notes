# Multi-Factor Delete (MFA delete)

Is a feature that adds an **extra layer of security to your S3 bucket** by requiring a user to authenticate using an MFA token before they can delete objects from the bucket

- To use MFA delete, Versioning must be enabled on the bucket
- **Only the bucket owner (root account) can enable/disable MFA delete**
- **Cannot be enabled in the UI. Only using the CLI**

Will be required to

- Permanently delete an object version
- Suspend versioning on the bucket

Won't be required to

- Enable versioning
- List deleted versions
