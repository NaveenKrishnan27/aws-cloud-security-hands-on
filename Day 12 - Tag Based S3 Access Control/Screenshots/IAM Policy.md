{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "AllowTaggedObjectAccess",
      "Effect": "Allow",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::day12-tagpolicy/*",
      "Condition": {
        "StringEquals": {
          "s3:ExistingObjectTag/Project": "Confidential"
        }
      }
    },
    {
      "Sid": "AllowBucketListing",
      "Effect": "Allow",
      "Action": "s3:ListBucket",
      "Resource": "arn:aws:s3:::day12-tagpolicy"
    }
  ]
}
 