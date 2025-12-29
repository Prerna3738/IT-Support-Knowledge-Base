Bug Report: Database Connection Timeout in App v2.4
Status: Escalated to Tier 3 / Dev Team Priority: High

Issue Summary

Users are reporting a "504 Gateway Timeout" when attempting to generate monthly reports.

Steps to Reproduce

Log into User Portal.

Navigate to 'Reports' -> 'Generate Monthly Summary'.

Process hangs at 45% and fails after 60 seconds.

Initial Investigation (Tier 2)

Log Analysis: Checked server.log; found java.sql.SQLTimeoutException.

Resource Check: Server CPU is at 15%, but Database connections are maxed at 100/100.

Temporary Workaround: Restarting the connection pool restores service for 30 minutes.
