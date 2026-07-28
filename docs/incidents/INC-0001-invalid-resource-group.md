# INC-0001: Invalid resource group query

## Severity

SEV-4

## Impact

No customer impact. The operator could not retrieve the expected resource group.

## Symptoms

The Azure CLI returned an error when querying a resource group.

## Investigation

- Confirmed the Azure CLI session was authenticated.
- Listed the available resource groups.
- Compared the requested name with the deployed name.
- Used `az group exists` to validate both names.

## Root cause

The operator used `prod` instead of `dev` in the resource group name.

## Resolution

Used the correct resource group name.

## Preventive action

Copy resource names from validated command output and use variables in scripts.