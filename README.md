Exercise 1 — Dynamic blocks from a typed variable (Advanced)

Task: Define a variable rules of type list(object({ description=string, port=number, cidr=string })). Build one security group whose ingress rules are generated entirely by a dynamic block. Add a validation block that rejects any port outside 1–65535. Prove the validation works by passing an invalid value.

Exercise 2 — Multi-region with provider aliases (Advanced)
Task: Configure two aws providers: default in ap-southeast-1 and an alias aws.tokyo in ap-northeast-1. Create one S3 bucket in each region. Then wrap the bucket in a module and pass the aliased provider into a second module call so the module itself is region-agnostic.

Exercise 3 — Refactor safely with moved blocks (Advanced)
Task: Start from a resource aws_s3_bucket.old and a working apply. Rename it to aws_s3_bucket.new AND move it into a module in the same change. Use moved {} blocks so terraform plan shows a move (not destroy+create). Confirm the plan reports zero resources to add or destroy.
