
---

### 📄 `certs/acm-setup.md`

```markdown
# SSL Setup Using AWS Certificate Manager (ACM)

## Objective
Enable HTTPS on your Application Load Balancer using a valid SSL certificate from ACM.

## Steps

1. Go to AWS Certificate Manager → **Provision Certificate** → Request a public certificate.
2. Enter your domain name:xxxxxx  
3. Choose DNS validation.
4. Copy the CNAME validation record provided by ACM.
5. Add it to your GoDaddy DNS records:
- **Type**: CNAME
- **Name** and **Value**: Paste exactly as provided by ACM.

6. Wait for ACM to validate the domain (can take a few minutes).
7. Once status shows **Issued**, go to your ALB:
- Edit the listener on port **443 (HTTPS)**
- Add the ACM certificate

## Result
- Your app is now served over HTTPS using a valid certificate from ACM.

