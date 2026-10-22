# Incident Report 01: Web Server Unavailable

## Status
Simulated training incident — not an observed AWS outage.

## Scenario
A website hosted on a Linux server becomes unavailable to users.

## Symptoms
- The browser cannot load the website.
- The web service may be stopped or the expected port may not be listening.
- Network rules may prevent legitimate traffic from reaching the server.

## Investigation Steps
1. Confirm the reported URL and error message.
2. Check server reachability and instance status, if applicable.
3. Check the web service using `systemctl status nginx` on a Linux system where Nginx is installed.
4. Review service logs using `journalctl -u nginx --since '30 minutes ago'`.
5. Check listening ports using `ss -tuln`.
6. Review the relevant firewall and cloud security-group rules.

## Example Root Cause
For this training scenario, assume Nginx was stopped unexpectedly. This is a hypothetical cause, not a verified finding.

## Remediation
On an authorized test system, start the service with `sudo systemctl start nginx`, if Nginx is installed and its configuration is valid.

## Validation
- Confirm the service is active.
- Test the local endpoint using `curl -I http://localhost` where applicable.
- Test external connectivity only if the server is intentionally exposed and authorized.
- Review logs and monitoring metrics for further errors.

## Prevention
- Monitor service health and relevant metrics.
- Configure suitable alerts.
- Review service restart policies and deployment changes.

## Lessons Learned
Use evidence to distinguish service failures from DNS, routing, firewall, and application problems. Never assume the root cause before investigation.
