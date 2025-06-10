# Day 05 – Fine-grained S3 Access Policies

## ✅ What I Did
- Attached IAM policy to access specific bucket
- Added `s3:ListAllMyBuckets` for bucket visibility
- Tested allow vs deny rules

## 🧠 Key Learnings
- Deny overrides Allow
- Must include `s3:ListAllMyBuckets` to see the bucket

## 📸 Screenshots
Screenshots of policy and bucket visibility tests in `screenshots/`.
