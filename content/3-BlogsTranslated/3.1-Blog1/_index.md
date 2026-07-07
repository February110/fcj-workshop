---
title: "Subdomain Takeover"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# Subdomain Takeover: When a Forgotten DNS Record Becomes an Attack Vector

This blog explains how Subdomain Takeover can happen when a DNS record remains active after the AWS resource behind it has been deleted. For example, a Route 53 record may still point to an old S3 static website endpoint, CloudFront distribution, Elastic Beanstalk environment, or another cloud service that no longer exists.

When the original resource is removed but the DNS record remains, an attacker may be able to recreate or claim a compatible resource and serve content under the abandoned subdomain. This turns a simple cleanup mistake into a security risk.

## Main Points

* A dangling DNS record is a common root cause of subdomain takeover.
* The risk is higher when DNS records are not reviewed after deleting S3 buckets, CloudFront distributions, or application environments.
* Route 53 should be treated as part of the attack surface, not only as a networking component.
* Detection can be automated by comparing DNS records with real resources in the AWS account.

## AWS-Based Detection Idea

The proposed detection workflow uses AWS services:

1. AWS Config records changes to supported resources.
2. Lambda checks Route 53 hosted zones and DNS records.
3. The function compares DNS targets with existing resources such as S3, CloudFront, and Elastic Beanstalk.
4. If a dangling record is found, the system sends a finding to Security Hub and sends a notification through SNS.

## Lessons Learned

Subdomain takeover is preventable when teams maintain DNS hygiene. Every deleted resource should trigger a DNS review, and DNS records should be monitored continuously instead of only checked during initial deployment.
