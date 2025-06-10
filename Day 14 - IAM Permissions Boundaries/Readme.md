# Day 14 – IAM Permissions Boundary

## ✅ What I Did
- Created a custom IAM permissions boundary that only allows S3 actions  
- Created an IAM user with a policy allowing both S3 and EC2  
- Attached the permissions boundary to the user  
- Verified S3 access works and EC2 access is denied using AWS CLI  

## 🧠 Key Learnings
- Permissions boundaries define the maximum allowed permissions  
- Even if IAM policies grant access, boundaries can restrict it further  
- Effective permissions = IAM policy ∩ permissions boundary  
- Useful for managing over-permissioning in large environments  

## 📸 Screenshots
Screenshots of boundary policy, IAM user setup, CLI results in `screenshots/`
