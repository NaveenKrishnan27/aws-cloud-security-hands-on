# Day 03 – Simulating IAM Role Assumption

## ✅ What I Did
- Created a custom IAM role with S3 access
- Created trust relationship for EC2 only
- Tried to assume role as IAM user

## 🧠 Key Learnings
- Role assumption fails if trust policy denies it
- `AccessDenied` error when IAM user tries assuming EC2-trusted role

## 📸 Screenshots
Find all test results and errors in `screenshots/`.
