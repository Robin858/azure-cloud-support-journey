# Day 03 - Microsoft Entra ID and Azure RBAC

## Business scenario

TicoCloud Solutions received a request for read-only access to a
development environment.

## Objectives

- Identify the signed-in principal
- Understand Azure RBAC
- Review built-in roles
- Analyze inherited access
- Apply least privilege
- Design a read-only access assignment

## Authentication vs. authorization

Explain the difference in your own words.

## Security principals

Explain:

- User
- Group
- Service principal
- Managed identity

## RBAC assignment anatomy

Explain:

- Security principal
- Role definition
- Scope

## Scope hierarchy

Document the four Azure RBAC scope levels.

## Role comparison

Compare:

- Reader
- Contributor
- Owner

## Effective access and inheritance

Explain why a role assigned at subscription scope can apply to a
resource group.

## Access request decision

Document the recommended principal, role, and scope.

## Troubleshooting

Explain how you would investigate a user who can authenticate but
cannot view the resource group.

## Lessons learned

1. How to list all the Azure role
2. How to define wich role I can assign
3. Practice some command of Azure CLI

## Cost and cleanup

No billable resources were deployed.
The temporary resource group was deleted.

## English summary

Write at least six short sentences.

Importante: Azure RBAC frente a roles de Microsoft Entra ID

Estos dos sistemas están relacionados, pero no son iguales.

Azure RBAC

Administra acceso a recursos de Azure:

Virtual machines
Virtual networks
Storage accounts
Resource groups
Subscriptions

Ejemplo:
Reader on rg-application-dev-001

Microsoft Entra roles

Administran funciones del directorio:

Usuarios
Grupos
Aplicaciones
Configuración de identidad
Administración del tenant

Ejemplo:
User Administrator

Tener permisos para administrar una VM no significa tener permisos para administrar usuarios del tenant.

Tener permisos para administrar usuarios de Entra tampoco significa automáticamente poder administrar máquinas virtuales.

## English summary
Today I learned the difference between authentication and authorization. I practice some Azure CLI commands about RBAC, I understand the importance to give the minimum possible privilege.