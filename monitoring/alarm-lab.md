# AWS CloudWatch Monitoring Lab

## Objective
Document how AWS CloudWatch helps monitor infrastructure and identify operational problems.

## Key Concepts
- **Metrics:** Measurements such as EC2 CPU utilization.
- **Alarms:** Rules that evaluate metrics against configured thresholds.
- **Notifications:** Amazon SNS can send notifications when an alarm changes state, when configured.
- **Dashboards:** Visualize important metrics in one place.

## Proposed CPU Alert
- Metric: EC2 CPUUtilization
- Evaluation: Review the metric over consecutive periods.
- Example threshold: CPU utilization above 80% for 5 minutes.
- Intended response: Investigate processes, traffic, and application logs before taking action.

## Troubleshooting Procedure
1. Check the alarm state and metric timestamps.
2. Review instance status checks.
3. Inspect CPU usage and application logs.
4. Identify the likely cause.
5. Apply a corrective action and verify recovery.

## Cost and Validation Notes
This file documents a proposed lab configuration. No AWS alarm or notification has been created yet. Verify current CloudWatch pricing and the account's Free Tier eligibility before deploying resources.

## Results
To be completed after testing with actual metrics or a clearly labeled simulation.
