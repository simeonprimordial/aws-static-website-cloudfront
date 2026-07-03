# Lessons Learned

- CloudFront caches content at edge locations.
- S3 should remain private when using OAC.
- Versioning protects against accidental overwrites.
- Cache invalidation forces CloudFront to fetch updated content.
- Static websites do not require EC2 instances.