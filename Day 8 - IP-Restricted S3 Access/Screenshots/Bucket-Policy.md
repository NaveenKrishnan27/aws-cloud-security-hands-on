{
	"Version": "2012-10-17",
	"Statement": [
		{
			"Sid": "ExplicitDenyFromUnapprovedIPs",
			"Effect": "Deny",
			"Principal": {
				"AWS": "arn:aws:iam::069074629172:user/normal-user"
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
					"aws:SourceIp": "49.207.177.87/32"
				}
			}
		},
		{
			"Sid": "AllowSpecificUserFromApprovedIP",
			"Effect": "Allow",
			"Principal": {
				"AWS": "arn:aws:iam::069074629172:user/normal-user"
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
					"aws:SourceIp": "49.207.177.87/32"
				}
			}
		}
	]
}