# 🆔 IAM

## IAM user group

Groups let us specify permission for multiple users. `Identity based policies` can be attached to a group

* IAM user group is a collection of IAM users
* User groups can't be nested

## IAM Roles

Used when AWS services need to perform action on users behalf. Permissions to AWS Services are assigned with IAM Roles. Policies are attached to one principal, however, Roles can be asssumed by anyone. .

Roles can be used by:

* IAM user in the same AWS account as the role
* IAM user in a different AWS account
* A web service offered by AWS like EC2
* An external user authenticated by an external identity provider

Example Roles:

* EC2 instance roles
* Lambda function roles
* Cloudformation roles

## IAM Policy

Policies are used to manage access in AWS. Policies can be attached to IAM Identities (User, Group, or roles). Policies are evaluated when an IAM Principlpe (user / role) makes a request.

Policy Types:

* **Identitiy based policies**: Attached to IAM identities (User/Group/Roles)

<details>

<summary>Managed Policies</summary>

* AWS Managed Policies: Created & managed by AWS
* Customer managed policies: Created and managed by AWS account

</details>

<details>

<summary>Inline Policies</summary>

Policies that are added to single user, group or role. Maintain a strict one-to-one relationship between a policy & entity. They are deleted when you delete the idenitity.&#x20;

</details>

* **Resource based policies**: Attached to resources
* Permission boundaries: Defines maximum permission that identity based policies can grant to an IAM Entity (User / Role)
* Organizations SCP:&#x20;
* Access Control List (ACL):
* Session Policies:

## IAM Security Tools

#### IAM Credential Report (Account Level):

* A report that lists all account users & status of their credentials

#### IAM  Access Advisor (user-level):

* Shows service permissions granted to a user and when those services were last accessed
