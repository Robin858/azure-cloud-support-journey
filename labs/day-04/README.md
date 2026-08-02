# Day 04 - Azure Virtual Network Fundamentals

## Business Scenario

TicoCloud Solutions required a segmented virtual network for a
three-tier development application.

## Objectives

- Review IPv4 and CIDR
- Create an Azure virtual network
- Create web, application, and data subnets
- Investigate an overlapping subnet
- Create and associate network security groups
- Define basic traffic rules

## Network Design

| Component | Address Prefix |
|---|---|
| VNet | 10.20.0.0/16 |
| Web subnet | 10.20.1.0/24 |
| Application subnet | 10.20.2.0/24 |
| Data subnet | 10.20.3.0/24 |

## Segmentation Decision

Explain why the three application tiers use separate subnets.

## Network Security Groups

Document:

- NSG name
- Associated subnet
- Allowed source
- Destination port
- Business purpose

## Incident INC-0004

### Symptom

The test subnet deployment failed.

### Proposed Prefix

`10.20.1.128/25`

### Investigation

Describe how the existing VNet and subnet prefixes were reviewed.

### Root Cause

Explain the address overlap.

### Resolution

Document the valid prefix used and the cleanup performed.

## NSG Rule Analysis

Explain:

- Direction
- Priority
- Source
- Destination
- Port
- Protocol
- Access

## Troubleshooting Notes

Explain why an NSG Allow rule does not prove that an application is
available.

## Lessons Learned

1.
2.
3.

## Cost and Cleanup

No virtual machines or public IP addresses were deployed.

The temporary resource group and all network resources were deleted.

## English Summary

Write at least seven short sentences.