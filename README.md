# AWS IAM Access Control 

This project demonstrates IAM least privilege design using AWS IAM users, groups, custom policies, and S3 access control testing.

## Project Overview

The lab simulates a small cloud environment with three user roles:

- `dev-user`: can read and upload files only inside the `dev/` prefix.
- `intern-user`: has restricted access and cannot upload files.
- `auditor-user`: can view IAM/S3 configuration but cannot read S3 object content.

The goal is to verify that each user only receives the permissions required for their responsibility.

## Security Controls Implemented

- Root MFA enabled
- No root access keys
- S3 Block Public Access enabled
- Custom IAM policies
- IAM groups for role-based access control
- Allow/Deny permission testing
- Sensitive information redacted from screenshots


## Test Summary

| User         | Test                   | Expected  | Actual |
|--------------|------------------------|-----------|--------|
| dev-user     | Read dev/dev.txt       | Allow     | Allow  |
| dev-user     | View bucket versioning | Deny      | Deny   |
| intern-user  | Upload to dev/         | Deny      | Deny   |
| auditor-user | View IAM dashboard     | Allow     | Allow  |
| auditor-user | Read S3 object content | Deny      | Deny   |

