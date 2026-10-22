# AWS IAM and Network Security Lab

## Objective
Understand how AWS identity permissions and network controls help protect cloud infrastructure.

## IAM Fundamentals
- **IAM users and roles:** Identities used to access AWS resources.
- **Policies:** JSON documents that define allowed or denied actions.
- **Least privilege:** Grant only the permissions required for a task.
- **MFA:** Adds an extra authentication factor to supported sign-in workflows.
- **Root user:** Avoid using root for routine administration; protect it with MFA.

## Network Security Fundamentals
- **VPC:** A logically isolated AWS network.
- **Subnet:** A range of IP addresses within a VPC.
- **Route table:** Determines where network traffic is directed.
- **Security group:** Stateful virtual firewall associated with supported resources.
- **Network ACL:** Stateless subnet-level traffic filter.

## Example Web Server Rules
- HTTP, TCP port 80: Allow only when required for a public website.
- HTTPS, TCP port 443: Allow only when required for secure web access.
- SSH, TCP port 22: Never expose broadly to the internet for routine administration; prefer Systems Manager Session Manager when configured and available.

## Security Review Checklist
1. Check that identities have only necessary permissions.
2. Confirm MFA is enabled for privileged access.
3. Review inbound and outbound security-group rules.
4. Avoid storing access keys or passwords in GitHub.
5. Review audit logs and investigate unexpected access.

## Results
This document records learning objectives and proposed checks. Add evidence after validating the controls in an AWS account or a clearly labeled local simulation.
