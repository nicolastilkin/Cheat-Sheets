# ☁️ AWS

## 🛠️ CLI Configuration

| Action                 | Command                                  |
| ---------------------- | ---------------------------------------- |
| Configure AWS CLI      | `aws configure`                          |
| Set profile            | `aws configure --profile <profile-name>` |
| Use profile in command | `aws s3 ls --profile <profile-name>`     |
| Set region             | `--region <region>`                      |

---

## 📦 S3 (Simple Storage Service)

| Action               | Command                                             |
| -------------------- | --------------------------------------------------- |
| List buckets         | `aws s3 ls`                                         |
| List bucket contents | `aws s3 ls s3://<bucket-name>`                      |
| Upload file          | `aws s3 cp <file> s3://<bucket-name>/`              |
| Download file        | `aws s3 cp s3://<bucket-name>/<file> <destination>` |
| Sync folders         | `aws s3 sync <local-dir> s3://<bucket-name>/`       |
| Remove object        | `aws s3 rm s3://<bucket-name>/<file>`               |

---

## 🖥️ EC2 (Elastic Compute Cloud)

| Action             | Command                                           |
| ------------------ | ------------------------------------------------- |
| List instances     | `aws ec2 describe-instances`                      |
| Start instance     | `aws ec2 start-instances --instance-ids <id>`     |
| Stop instance      | `aws ec2 stop-instances --instance-ids <id>`      |
| Reboot instance    | `aws ec2 reboot-instances --instance-ids <id>`    |
| Terminate instance | `aws ec2 terminate-instances --instance-ids <id>` |
| List AMIs          | `aws ec2 describe-images --owners self`           |

---

## 🔐 IAM (Identity & Access Management)

| Action                | Command                                                      |
| --------------------- | ------------------------------------------------------------ |
| List users            | `aws iam list-users`                                         |
| Create user           | `aws iam create-user --user-name <name>`                     |
| Attach policy to user | `aws iam attach-user-policy --user-name <name> --policy-arn <arn>` |
| List roles            | `aws iam list-roles`                                         |
| Create role           | `aws iam create-role --role-name <name> --assume-role-policy-document file://trust-policy.json` |
| List policies         | `aws iam list-policies`                                      |

---

## 🛡️ Security Groups

| Action                | Command                                                      |
| --------------------- | ------------------------------------------------------------ |
| List security groups  | `aws ec2 describe-security-groups`                           |
| Create security group | `aws ec2 create-security-group --group-name <name> --description "desc"` |
| Add rule              | `aws ec2 authorize-security-group-ingress --group-id <id> --protocol tcp --port 22 --cidr 0.0.0.0/0` |

---

## 🧠 CloudWatch

| Action          | Command                                                      |
| --------------- | ------------------------------------------------------------ |
| List metrics    | `aws cloudwatch list-metrics`                                |
| Get metric data | `aws cloudwatch get-metric-statistics --metric-name CPUUtilization --start-time <start> --end-time <end> --period 300 --namespace AWS/EC2 --statistics Average --dimensions Name=InstanceId,Value=<id>` |
| Create alarm    | `aws cloudwatch put-metric-alarm --alarm-name <name> ...`    |

---

## 📜 Logs (CloudWatch Logs)

| Action           | Command                                                      |
| ---------------- | ------------------------------------------------------------ |
| List log groups  | `aws logs describe-log-groups`                               |
| List log streams | `aws logs describe-log-streams --log-group-name <name>`      |
| Get logs         | `aws logs get-log-events --log-group-name <group> --log-stream-name <stream>` |

---

## 🧾 Billing & Cost

| Action         | Command                                                      |
| -------------- | ------------------------------------------------------------ |
| Get cost usage | `aws ce get-cost-and-usage --time-period Start=YYYY-MM-DD,End=YYYY-MM-DD --granularity MONTHLY --metrics "UnblendedCost"` |

---

## 🧪 Misc

| Action                  | Command                               |
| ----------------------- | ------------------------------------- |
| List regions            | `aws ec2 describe-regions`            |
| List availability zones | `aws ec2 describe-availability-zones` |
| Get caller identity     | `aws sts get-caller-identity`         |

---

## 📝 Sample Policy (JSON)

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "s3:*",
      "Resource": "*"
    }
  ]
}