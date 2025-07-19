{
	"Version": "2012-10-17",
	"Statement": [
		{
			"Sid": "ExplicitDenyFromUnapprovedIPs",
			"Effect": "Deny",
			"Principal": {
				"AWS": "arn:aws:iam::<ID>:user/normal-user"
			},
			"Action": [
				"s3:GetObject",
				"s3:ListBucket"
			],
			"Resource": [
				"arn:aws:s3:::day-8-bucket",
				"arn:aws:s3:::day-8-bucket/*"
			],
			"Condition": {
				"NotIpAddress": {
					"aws:SourceIp": <SourceIP>
				}
			}
		},
		{
			"Sid": "AllowSpecificUserFromApprovedIP",
			"Effect": "Allow",
			"Principal": {
				"AWS": "arn:aws:iam::<ID>:user/normal-user"
			},
			"Action": [
				"s3:GetObject",
				"s3:ListBucket"
			],
			"Resource": [
				"arn:aws:s3:::day-8-bucket",
				"arn:aws:s3:::day-8-bucket/*"
			],
			"Condition": {
				"IpAddress": {
					"aws:SourceIp": <SourceIP>
				}
			}
		}
	]
}