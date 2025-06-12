# Day 15 – IAM Policy Conditions: Time-Based Access Control

## ✅ What I Did
- Created an IAM user with time-based S3 access restrictions  
- Defined a custom policy using `aws:CurrentTime` to allow access between 9 AM and 6 PM UTC  
- Attached the policy to the user  
- Tested S3 access within and outside the allowed timeframe using AWS CLI  

## 🧠 Key Learnings
- IAM policies can restrict access based on time using `DateGreaterThan` and `DateLessThan`  
- `aws:CurrentTime` is evaluated in UTC regardless of user or resource region  
- Time-based conditions are useful for enforcing business hours or restricting off-hours access  

## 📸 Screenshots
Policy JSON, IAM user setup, and CLI results in `screenshots/`
