# Troubleshooting

## Issue

Access Denied

Cause

Bucket Policy missing.

Solution

Attach the CloudFront-generated bucket policy.

---

## Issue

CSS not loading.

Cause

Incorrect object path.

Solution

Verify styles.css is in the bucket root.

---

## Issue

Old page still displayed.

Cause

CloudFront cache.

Solution

Create a cache invalidation.