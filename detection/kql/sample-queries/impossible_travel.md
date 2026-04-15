# Impossible Travel KQL Starter

```kusto
// Adjust tables and fields to your environment
SigninLogs
| where ResultType == 0
| project TimeGenerated, UserPrincipalName, IPAddress, Location, AppDisplayName
| order by UserPrincipalName asc, TimeGenerated desc
```

Use this as a starting point. Pair with enrichment before alerting.
