# HelloID-Task-SA-Source-ActiveDirectory-GroupGetAccountMemberships

## Prerequisites

- [ ] The HelloID SA on-premises agent installed
- [ ] The ActiveDirectory module is installed on the server where the HelloID SA on-premises agent is running.
- [ ] Data source input parameter (required parameter) named `selectedGroup`. The linked form-element should at least return a model containing the `name` property


## Description

This code snippet executes the following tasks:

1. Define `$groupName` based on the `selectedGroup` data source input `$datasource.selectedGroup.name`
2. Imports the ActiveDirectory module.
3. Retrieve the AD group using the `Get-ADgroup` cmdlet.
4. Get the AD account memberships of the AD group using the `Get-ADGroupMember` cmdlet.
5. Return a hash table for each account membership using the `Write-Output` cmdlet.

> To view an example of the data source output, please refer to the JSON code pasted below and select the `Interpreted as JSON` option in HelloID

```json
{
    "name": "All Managers"
}
```