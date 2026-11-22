
# AZ-104 — Part 1: Manage Azure Identities and Governance

## 1. Microsoft Entra ID
- Cloud-based identity and access management service.
- Manages users, groups, devices and applications.
- Authentication = verifies who you are.
- Authorization = determines what you can do.
- A tenant is the organisation's dedicated identity directory.

## 2. Users and Groups
- Member: internal organisation user.
- Guest: external user invited to collaborate.
- Security groups: manage access and permissions.
- Microsoft 365 groups: support collaboration.
- Assigned membership: users are added manually.
- Dynamic membership: users are added based on attribute rules.

## 3. Azure Resource Hierarchy
Management Groups → Subscriptions → Resource Groups → Resources

- Management Groups: organise multiple subscriptions.
- Subscriptions: billing and resource-management boundaries.
- Resource Groups: logical containers for related resources.
- Resources: actual Azure services, such as VMs and storage accounts.
- Deleting a Resource Group normally deletes its resources.

## 4. Azure Policy
- Controls and enforces resource configurations.
- Policy definition: describes a rule.
- Policy assignment: applies the rule to a scope.
- Initiative: collection of policy definitions.
- Deny: blocks non-compliant requests.
- Audit: reports non-compliance without blocking.
- Modify: changes resource properties.
- DeployIfNotExists: deploys missing related resources or configurations.

**Policy vs RBAC:**
- Policy = what configurations are allowed?
- RBAC = who can perform actions?

## 5. Azure RBAC
Controls who can access Azure resources and what they can do.

Three elements of a role assignment:
1. Security principal = WHO (user, group, service principal or managed identity).
2. Role definition = WHAT permissions.
3. Scope = WHERE permissions apply.

Common roles:
- Reader: view resources.
- Contributor: manage resources but cannot grant access.
- Owner: full access, including granting access.
- User Access Administrator: manage access assignments.

Scopes: Management Group → Subscription → Resource Group → Resource.

Permissions are generally inherited by child scopes.

## 6. Self-Service Password Reset (SSPR)
- Allows users to reset their own passwords.
- Administrators configure who can use SSPR.
- Users must register authentication methods.
- Password writeback synchronises cloud password resets with on-premises Active Directory in hybrid environments.

## Important Exam Distinctions
- Authentication vs Authorization.
- Entra directory roles vs Azure RBAC roles.
- Azure Policy vs Azure RBAC.
- Security group vs Microsoft 365 group.
- Security principal vs Role definition vs Scope.
- Audit vs Deny.
