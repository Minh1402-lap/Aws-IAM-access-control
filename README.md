# Aws-IAM-access-control
## Test Summary

| User         | Test                   | Expected  | Actual |
|--------------|------------------------|-----------|--------|
| dev-user     | Read dev/dev.txt       | Allow     | Allow  |
| dev-user     | View bucket versioning | Deny      | Deny   |
| intern-user  | Upload to dev/         | Deny      | Deny   |
| auditor-user | View IAM dashboard     | Allow     | Allow  |
| auditor-user | Read S3 object content | Deny      | Deny   |
