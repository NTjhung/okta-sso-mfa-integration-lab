# Okta App Assignment Matrix

## Purpose

This document shows how application access is assigned in the Okta SSO and MFA lab. The goal is to demonstrate group-based application assignment and least privilege access planning.

## App Assignment Matrix

| Group | Application | Access Type | MFA Required | Reason |
|---|---|---|---|---|
| Okta-HR-Users | HR Portal | SSO | Yes | HR data may include employee information |
| Okta-Finance-Users | Finance App | SSO | Yes | Finance data is sensitive |
| Okta-IT-Admins | Admin Tools | SSO/Admin Access | Yes | Admin access requires stronger security |
| Okta-Contractors | Project App | Limited SSO | Yes | Contractor access should be limited and monitored |
| Okta-Sales-Users | Sales App | SSO | No | Standard sales access in this lab scenario |
| Okta-MFA-Required | All sensitive apps | MFA enforcement group | Yes | Used to apply stronger authentication requirements |

## Access Assignment Rules

1. Application access should be assigned through groups when possible.
2. Users should only receive access required for their role.
3. Sensitive applications should require MFA.
4. Contractor access should be limited and reviewed regularly.
5. Admin application access should require stronger authentication.
6. Group membership should be reviewed during access reviews.

## Example App Access

| User | Department | Group | Application Access |
|---|---|---|---|
| Alice Johnson | HR | Okta-HR-Users | HR Portal |
| Brian Lee | Finance | Okta-Finance-Users | Finance App |
| Carlos Ramirez | IT | Okta-IT-Admins | Admin Tools |
| Dana Smith | Contractors | Okta-Contractors | Project App |
| Emma Wilson | Sales | Okta-Sales-Users | Sales App |

## Least Privilege Notes

The principle of least privilege means users should only have the access needed for their current job. Group-based application assignment helps reduce manual errors and keeps access easier to review.
