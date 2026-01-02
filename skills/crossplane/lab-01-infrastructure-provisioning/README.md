# Crossplane Infrastructure Provisioning Lab

## Lab Overview
**Skill Level**: Advanced  
**Duration**: 6-8 hours initial setup + refinement  
**Crossplane Version**: 1.15+ (Modern API)  
**Business Value**: Multi-cloud abstraction and self-service infrastructure  
**Author**: Willem van Heemstra
**Link**: [Crossplane Infrasructure Provisioning](https://github.com/crossplane-infrastructure-provisioning)
---

## Business Problem

Organizations struggle with multi-cloud infrastructure management, leading to:
- **Cloud vendor lock-in** - difficult to migrate between providers
- **Inconsistent provisioning** - different tools and processes per cloud
- **Slow deployment cycles** - manual infrastructure provisioning takes days/weeks
- **Developer bottlenecks** - infrastructure teams become gatekeepers
- **Configuration drift** - manual changes lead to undocumented infrastructure

## Solution

This lab demonstrates a **Crossplane-based Infrastructure as Code (IaC)** solution that:
1. Provides a unified API for multi-cloud infrastructure provisioning
2. Enables developer self-service through declarative Kubernetes manifests
3. Ensures consistency across Azure, AWS, and GCP
4. Implements GitOps workflows for infrastructure deployment
5. Reduces provisioning time from days to minutes

## What's Different in Crossplane v1.15+

**Modern API** (no separate claims needed):
- Direct use of Composite Resources (XR)
- Simplified API surface
- Cleaner developer experience
- Same functionality, less complexity

**Old way (v1.14 and earlier)**:
```yaml
# Required separate Claim resource
apiVersion: database.example.com/v1alpha1
kind: DatabaseInstance  # Claim
