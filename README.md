# AWS-CIS-sentinel
Pre-written Sentinel policies are ready to use compliance checks for CIS AWS Foundations Benchmarking v1.2, v1.4 and v3.0 to help enable your AWS resources meet industry security standards.

If you want to enable only a subset of the policies or change the enforcement levels to either **soft-mandatory** or **hard-mandatory**, we recommend updating the contents of the sentinel.hcl file in each library before applying the Terraform configuration.

```
policy "iam-password-expiry" {
  source = "./policies/iam/iam-password-expiry.sentinel"
  enforcement_level = "advisory"
  params = {
    password_expiry_days = 90
  }
}
```

Credited by <https://github.com/hashicorp/policy-library-CIS-Policy-Set-for-AWS-Terraform>
