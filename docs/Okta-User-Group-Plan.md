# Okta User and Group Plan

## Purpose

This document defines the users and groups used in the Okta SSO and MFA lab. The goal is to show how group-based access can be used to assign application access and apply authentication requirements.

## Lab Users

| User | Department | Job Title | Group |
|---|---|---|---|
| Alice Johnson | HR | HR Manager | Okta-HR-Users |
| Brian Lee | Finance | Finance Analyst | Okta-Finance-Users |
| Carlos Ramirez | IT | Helpdesk Technician | Okta-IT-Admins |
| Dana Smith | Contractors | Project Contractor | Okta-Contractors |
| Emma Wilson | Sales | Sales Representative | Okta-Sales-Users |

## Lab Groups

| Group | Purpose |
|---|---|
| Okta-HR-Users | HR department access |
| Okta-Finance-Users | Finance department access |
| Okta-IT-Admins | IT/admin access |
| Okta-Contractors | Contractor access |
| Okta-Sales-Users | Sales department access |
| Okta-MFA-Required | Users who require MFA |

## Group-Based Access Rules

1. Users should be assigned to groups based on department or role.
2. Application access should be assigned to groups when possible.
3. Contractor access should be limited and reviewed regularly.
4. Finance and IT admin access should require stronger authentication.
5. MFA should be required for sensitive or privileged access.

## Least Privilege Notes

Users should only receive access required for their role. Group-based access helps reduce manual errors and supports least privilege by standardizing application assignment.
