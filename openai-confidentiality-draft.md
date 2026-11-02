# Confidentiality and Know-how Protection When Using ChatGPT and Codex

**Version:** 0.5 — governance, adoption guidance and ISO/NIST/EU AI Act mapping; technical chapters remain in draft\
**Date:** 2 November 2026  
**Audience:** Business owners, technology leaders, security teams and legal advisers  
**Status:** Working draft; proposed controls and policy require organizational approval and technical validation.

## Introduction

ChatGPT and Codex can help a business analyse documents, develop software and explore new ideas. These activities can also disclose customer information, source code, commercial strategies and unpublished research to external systems. The business question is how to obtain useful assistance while retaining control over who receives this information, how it is used and how long it remains available.

This document focuses on OpenAI: ChatGPT, Codex and the OpenAI API. LiteLLM, network firewalls, HTTP proxies and Data Loss Prevention (DLP) are considered as controls around access to OpenAI, not as alternative model providers. Oracle Cloud Infrastructure (OCI) is considered as a possible hosting and network enforcement environment.

This guide addresses one control domain within wider AI governance: confidentiality and control of business know-how when using OpenAI. It supports decisions about permitted information, services, access routes and accountable owners. An organization-wide AI inventory is an input to this assessment; this document does not govern the full AI portfolio or establish compliance or certification.

Confidentiality approval does not approve output accuracy, fairness, intellectual-property rights or autonomous actions. The business owner must arrange the relevant quality, legal, privacy, security and operational reviews before relying on outputs or authorizing consequential actions. Chapter 4 identifies those handoffs. Appendix A maps this document to ISO/IEC 42001:2023, NIST AI RMF 1.0 and applicable EU AI Act provisions, with applicability decisions, evidence requirements and gaps.

The proposed approach combines company policy, technical enforcement and operational verification. A policy defines permitted information and uses. Technical controls restrict access and inspect supported data flows. Verification establishes whether those controls work in the actual deployment. None of these replaces an assessment of OpenAI's contractual commitments and the residual trust placed in the provider.

Each chapter opens with an introductory paragraph. Chapter 3 develops the earlier research findings, Chapter 4 defines the proposed governance approach, and Chapter 5 is developed from official OpenAI documents; the technical chapters retain sketches for further development. Source-based statements link to their supporting documents. Proposed company requirements are design decisions, not claims that a product already provides or enforces them. Chapter 4 sets out adoption patterns selected by information sensitivity and control requirements. For workflows requiring a company-controlled gateway, Chapter 11 considers LiteLLM with restrictions on unapproved direct access. LiteLLM and OCI are design options rather than prerequisites for every use case. The proposed architecture has not been implemented or tested.

## Table of Contents

### Part I — Business Challenges

- [Chapter 1 — Confidentiality and Business Assets](chapters/en/01-confidentiality-and-business-assets.md)

### Part II — Business Use Case: Confidential Research

- [Chapter 2 — Confidential Research and the Mathematics Dispute](chapters/en/02-confidential-research.md)
- [Chapter 3 — Research Findings and Business Lessons](chapters/en/03-research-findings-and-business-lessons.md)

### Part III — Governance: Addressing the Business Challenges

- [Chapter 4 — Governance: From Business Risk to Approval Criteria](chapters/en/04-governance.md)

### Part IV — Business Assets, Contracts and Company Policy

- [Chapter 5 — OpenAI Policy and Contract Perspective](chapters/en/05-openai-policy-and-contracts.md)
- [Chapter 6 — Draft Company Rules](chapters/en/06-company-rules.md)

### Part V — Technical Context and Protection Limits

- [Chapter 7 — Data Flows in ChatGPT and Codex](chapters/en/07-data-flows.md)
- [Chapter 8 — Accounts, Authentication and Service Boundaries](chapters/en/08-accounts-and-authentication.md)
- [Chapter 9 — Technical Protection and Its Limits](chapters/en/09-technical-protection.md)
- [Chapter 10 — Retention, Deletion and Zero Data Retention](chapters/en/10-retention-deletion-and-zdr.md)

### Part VI — Proposed Architecture and Enforcement

- [Chapter 11 — Proposed Architecture with LiteLLM](chapters/en/11-litellm-architecture.md)
- [Chapter 12 — Network Enforcement and OCI Network Firewall](chapters/en/12-network-enforcement-and-oci.md)
  - Planned coverage: DNS, HTTP proxy and firewall controls for browser, CLI and API access, including direct-access restrictions and bypass testing.
- [Chapter 13 — DLP and Agent Controls](chapters/en/13-dlp-and-agent-controls.md)

### Part VII — Validation, Operations and Incident Response

- [Chapter 14 — Validation, Operations and Incident Response](chapters/en/14-validation-and-incident-response.md)

### Appendices

- [Appendix A — ISO/IEC 42001, NIST AI RMF and EU AI Act Mapping](appendices/en/appendix-a-standards-and-regulatory-mapping.md)

### References

- [References](chapters/en/15-references.md)
