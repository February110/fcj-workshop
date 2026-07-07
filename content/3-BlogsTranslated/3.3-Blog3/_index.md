---
title: "EKS Pod Identity Session Policies"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# Session Policies in Amazon EKS Pod Identity

This blog introduces session policies in Amazon EKS Pod Identity. The feature helps teams apply more precise IAM permissions to Kubernetes workloads without creating a large number of separate IAM roles.

## Problem

In large Kubernetes environments, many applications run as separate pods and need different AWS permissions. Creating one IAM role for every small permission variation can become difficult to manage. At the same time, using a broad role for many pods weakens least privilege.

## How Session Policies Help

Session policies allow teams to narrow the effective permissions for a pod session. Instead of creating many IAM roles, teams can use a base role and attach a more specific policy at session time. This gives finer control while keeping IAM role management simpler.

## Benefits

* Reduces IAM role sprawl in large EKS clusters.
* Makes least privilege easier to apply per workload.
* Improves security by narrowing pod permissions.
* Keeps operational management simpler than creating many dedicated roles.

## Lessons Learned

EKS Pod Identity session policies are useful for teams that need both security and scalability. The feature gives platform teams a more flexible way to manage AWS permissions for Kubernetes workloads without losing control of least-privilege boundaries.
