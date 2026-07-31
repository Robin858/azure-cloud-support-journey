# REQ-0003: Read-only access request

## Request

An application developer needs to review the resources deployed in the
development environment.

## Required actions

- View resources
- Review resource configuration
- Confirm deployment status

## Actions not required

- Create resources
- Modify resources
- Delete resources
- Manage role assignments

## Recommended principal

Document whether access should be assigned to a user or group.

A the apps developers group.

## Recommended role

Document the role and justify the decision.

The recommended role is Read-only because they doesn't need to modify or delete anything.

## Recommended scope

Document the scope and justify the decision.

The recommended scope is the resource group.

## Roles rejected

Explain why Contributor and Owner are excessive.

These roles are excessive because they doesn't need to change anything, so to apply the minimun privilege policy we have to give the minimum possible role that provides access to complete their tasks.

## Validation plan

Explain how Cloud Operations should verify the resulting access.

We have to review that the role assigned was the correct checking the access of the principal.

## Review and removal

Explain when the access should be reviewed or removed.

We have to review that we give the correct access next to give the role, and when the apps developers finish to review the resources we have to remove the access.