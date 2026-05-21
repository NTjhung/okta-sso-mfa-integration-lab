# Okta Troubleshooting Notes

## Purpose

This document lists common Okta IAM troubleshooting scenarios. The goal is to show how an IAM analyst or IAM engineer might investigate user access, SSO, MFA, and group assignment issues.

## Scenario 1: User Cannot Access an Application

### Possible Causes

- User is not assigned to the correct Okta group
- Application is not assigned to the user's group
- User account is inactive or suspended
- User is using the wrong login URL
- Application assignment has not synced or applied yet

### Troubleshooting Steps

1. Search for the user in Okta.
2. Confirm the user account is active.
3. Review the user's group memberships.
4. Confirm the application is assigned to the correct group.
5. Check whether the user is assigned directly or through a group.
6. Ask the user to sign out and try again.
7. Document the issue and resolution.

---

## Scenario 2: User Is Prompted for MFA Unexpectedly

### Possible Causes

- User is part of an MFA-required group
- User is accessing a sensitive application
- Policy requires MFA based on app, group, or risk
- User is signing in from a new device or location

### Troubleshooting Steps

1. Confirm the user's group membership.
2. Review the MFA policy.
3. Check the application sign-on policy.
4. Confirm whether the app is considered sensitive.
5. Document whether the MFA prompt is expected or unexpected.

---

## Scenario 3: User Is Not Prompted for MFA

### Possible Causes

- User is not in the MFA-required group
- MFA policy does not apply to the application
- App assignment is incorrect
- Policy priority/order issue
- User is excluded from the policy

### Troubleshooting Steps

1. Confirm the user is in the correct group.
2. Confirm the app is covered by the MFA policy.
3. Review policy conditions.
4. Check for exclusions.
5. Test with another user in the same group.
6. Document the result.

---

## Scenario 4: Contractor Has Too Much Access

### Possible Causes

- Contractor is assigned to the wrong group
- Contractor has direct app assignments
- Contractor was not removed after project completion
- Access review was not completed

### Troubleshooting Steps

1. Review contractor group membership.
2. Review assigned applications.
3. Remove unnecessary direct assignments.
4. Confirm business need with the project owner.
5. Update the access review tracker.
6. Document the remediation.

---

## Scenario 5: Admin Access Needs Review

### Possible Causes

- Admin group membership was assigned permanently
- User changed job roles
- Privileged access was not reviewed recently
- Admin access was assigned outside the normal process

### Troubleshooting Steps

1. Review admin group membership.
2. Confirm the user still needs admin access.
3. Validate with the IT manager or system owner.
4. Remove unnecessary admin access.
5. Document the review decision.
6. Save evidence for audit.

## Summary

Okta troubleshooting often requires checking the user, group membership, app assignment, MFA policy, and sign-on behavior. Good IAM documentation helps reduce repeat issues and supports audit readiness.
