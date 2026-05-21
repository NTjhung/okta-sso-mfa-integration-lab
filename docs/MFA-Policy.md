# Okta MFA Policy

## Purpose

This document defines a basic MFA policy for the Okta SSO and MFA lab. The goal is to demonstrate how stronger authentication can be applied to users, groups, and sensitive applications.

## MFA Policy Goals

The goals of this MFA policy are to:

1. Protect sensitive applications.
2. Require stronger authentication for administrators.
3. Require MFA for contractors.
4. Reduce the risk of account compromise.
5. Support least privilege and identity security best practices.

## MFA Requirements by Group

| Group | MFA Required | Reason |
|---|---|---|
| Okta-HR-Users | Yes | HR data may include sensitive employee information |
| Okta-Finance-Users | Yes | Finance data is sensitive |
| Okta-IT-Admins | Yes | Admin access requires stronger protection |
| Okta-Contractors | Yes | Contractor access should be more tightly controlled |
| Okta-Sales-Users | No | Lower-risk access in this lab scenario |
| Okta-MFA-Required | Yes | Dedicated group for users requiring MFA |

## MFA Policy Rules

1. Admin users must complete MFA when accessing admin tools.
2. Finance users must complete MFA when accessing finance applications.
3. HR users must complete MFA when accessing HR applications.
4. Contractors must complete MFA when accessing assigned project applications.
5. Users in the Okta-MFA-Required group must complete MFA for sensitive access.
6. MFA failures should be reviewed and documented.

## Example MFA Scenarios

| Scenario | Expected Result |
|---|---|
| Finance user signs into Finance App | MFA required |
| IT admin signs into Admin Tools | MFA required |
| Contractor signs into Project App | MFA required |
| Sales user signs into Sales App | MFA not required in this lab scenario |
| User in Okta-MFA-Required signs into sensitive app | MFA required |

## Troubleshooting Notes

If a user cannot complete MFA, the IAM team should:

1. Confirm the user is assigned to the correct group.
2. Confirm the user is using an approved authenticator method.
3. Check for account lockout or sign-in issues.
4. Confirm the correct MFA policy applies.
5. Document the issue and resolution in a ticket.

## Security Notes

MFA should be required for sensitive and privileged access. Admin, finance, HR, and contractor access should receive stronger authentication controls than lower-risk standard access.
