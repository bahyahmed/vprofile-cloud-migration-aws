# GoDaddy DNS Setup to Map Domain to AWS ELB

## Prerequisites
- A purchased domain on GoDaddy (e.g. `vprofileapp.com`)
- Deployed Application Load Balancer (ALB) with a DNS name (e.g. `vprofile-alb-123456789.us-east-1.elb.amazonaws.com`)

## Steps
1. Log in to your GoDaddy account.
2. Go to "My Products" → "DNS" → "Manage DNS".
3. Under "Records", click **Add**:
   - **Type**: CNAME
   - **Name**: `www`
   - **Value**: `<your-ALB-DNS-name>`
   - **TTL**: Default (1 Hour)
4. (Optional) Add a forwarding rule from root domain (`@`) to `www`.

## Outcome
- Accessing `www.vprofileapp.com` will route traffic through the AWS ALB.

