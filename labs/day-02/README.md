# Day 02 - Resource Protection

## Business scenario

TicoCloud Solutions required a protected resource group for an internal lab environment.

## Objectives

- Use PowerShell variables
- Manage Azure tags
- Apply a CanNotDelete lock
- Investigate a failed deletion
- Clean up the environment

## Resources

- Resource group: rg-cloudjourney-dev-002
- Region: East US
- Lock type: CanNotDelete

## Tagging strategy

Explain the purpose of the tags used during the lab.

## Incident

The resource group deletion failed while a CanNotDelete lock was active.

## Investigation

Describe the commands and evidence used to validate:

- Resource group existence
- Azure CLI authentication
- Resource inventory
- Management locks

## Root cause

Describe the verified root cause.

## Resolution

Describe how the lock was removed and how cleanup was validated.

## Tags vs. locks vs. RBAC

Explain the difference in your own words.

## Lessons learned

1. Create and delete blocks.
2. How to see a error caused by a block.
3. Manage variables with Azure CLI.

## Cost and cleanup

No billable resources were deployed.
The resource group and its management lock were deleted.

## English summary

Write five short sentences about the lab.

1. It was a really good lab.
2. I want to make a real project, buy I think that I have to learn more before.
3. I am looking for a new job in the Cloud or TI department.
4. I am thinking to be for the AZ104 Azure certification in 10 months.
5. I am more comfortable with the CLI.