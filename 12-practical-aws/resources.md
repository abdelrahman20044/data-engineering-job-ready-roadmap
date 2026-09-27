# L12 Resources · Practical AWS

## Recommended path

Implement the default architecture from the level README. Use AWS service documentation during deployment and AWS Skill Builder only when a specific concept blocks implementation.

## Arabic / Egyptian

No Arabic resource is assigned as primary. Existing Cloud Practitioner knowledge already covers broad concepts; the learning gap is implementation and evidence.

## English alternatives

- [AWS Skill Builder](https://skillbuilder.aws/) — search for the current **Data Engineering on AWS** learning plan; dynamic links and sign-in requirements can change.
- [AWS Workshops](https://workshops.aws/) — choose one relevant hands-on lab only.
- AWS Immersion Day material — optional if accessible and aligned with the selected services.

## Practice / labs

- S3 raw/curated prefixes and lifecycle rule.
- Minimal IAM policy validated against the real workflow.
- Secret retrieval without static repository credentials.
- EC2-to-RDS connectivity with no public database access, or the documented single-EC2 cost fallback.
- CloudWatch log/metric evidence for one failure.
- Budget alert and complete teardown.

## Reference

- [Amazon S3 documentation](https://docs.aws.amazon.com/s3/)
- [IAM documentation](https://docs.aws.amazon.com/iam/)
- [Secrets Manager documentation](https://docs.aws.amazon.com/secretsmanager/)
- [CloudWatch documentation](https://docs.aws.amazon.com/cloudwatch/)
- [EC2 IAM roles](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/iam-roles-for-amazon-ec2.html)
- [RDS for PostgreSQL](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html)
- [VPC security groups](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-security-groups.html)

## Later / skip

- Later: infrastructure as code if repeated deployment or target jobs justify it.
- Skip another general certification path, broad tours of Glue/EMR/Redshift/Kinesis, and multi-account architecture.
- Do not substitute Lambda, Glue, EMR, Redshift or EKS merely to maximize logos; change the default architecture only when project constraints or repeated job evidence justify it.
