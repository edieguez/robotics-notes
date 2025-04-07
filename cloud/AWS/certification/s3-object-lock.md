# S3 Object Lock

Is a feature of **S3** that allows users to easily deploy and enforce compliance controls on individual objects via a lockable policy. **Versioning must be enabled**

- Adopt a WORM (Write Once Read Many) model
- Lockable policy that can be applied to **an object**

## Retention mode: compliance

- Object versions can't be overwritten or deleted by any user, including the root user
- Objects retention modes can't be changed and retention periods can't be shortened

## Retention mode: governance

- Most users can't overwrite or delete an object version or alter its lock settings
- Some users have special permissions to change the retention or delete the object

## Common for both modes

- `Retention period` protect the object for a fixed period, it can be extended
- `Legal hold` protects the object until the hold is removed
  - Can be freely placed and removed using the `s3:PutObjectLegalHold` IAM permission
