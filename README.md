Project Infrastructure & Deployment Guide
Architecture Overview

This application is deployed on AWS using a secure, scalable, and production-ready architecture.

Amazon EKS cluster deployed in private subnets

Application Load Balancer (ALB) deployed in public subnets

Amazon RDS PostgreSQL in private subnets

React (frontend) and Flask (backend) deployed as Kubernetes Deployments

Route53 + ACM for DNS management and HTTPS

IAM Roles for Service Accounts (IRSA) for secure AWS access

Horizontal Pod Autoscalers (HPAs) for workload autoscaling

High-Level Architecture Flow

User → Route53 → ALB (HTTPS) → EKS Services → Pods (React/Flask) → RDS PostgreSQL

Setup Instructions
1. Deploy Infrastructure

Provision AWS infrastructure using:

Terraform or

eksctl

This includes:

VPC (public & private subnets)

EKS cluster

Node groups

RDS PostgreSQL

IAM roles

ALB configuration
