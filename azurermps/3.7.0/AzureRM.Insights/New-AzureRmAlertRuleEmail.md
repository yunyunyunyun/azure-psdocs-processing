---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version:
schema: 2.0.0
updated_at: 03/11/2017 02:03 AM
ms.date: 03/11/2017
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Insights/v2.7.0/New-AzureRmAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Insights/v2.7.0/New-AzureRmAlertRuleEmail.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/04f63f6e685743ace2c57eb157574e34e8610b1c
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# New-AzureRmAlertRuleEmail

## SYNOPSIS
Creates an email action for an alert rule.

## SYNTAX

```
New-AzureRmAlertRuleEmail [[-CustomEmails] <String[]>] [-SendToServiceOwners] [<CommonParameters>]
```

## DESCRIPTION
The **New-AzureRmAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.

## EXAMPLES

### Example 1: Create an alert rule email action for service owners
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

This command creates an alert rule email action to send for its service owners when an alert rule is fired.

### Example 2: Create an alert rule email action for non-service owners
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

This command creates an alert rule email action for the specified email addresses, but not for the service owners.

### Example 3: Create an alert rule email action for service owners and non-service owners
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails "pattif@contoso.net" -SendToServiceOwners
```

This command creates an alert rule email action for the specified address and for its service owners.

## PARAMETERS

### -CustomEmails
Specifies a list of comma-separated e-mail addresses.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SendToServiceOwners
Indicates that this operation sends an e-mail to the service owners when the rule fires.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-AzureRmLogAlertRule](./Add-AzureRmLogAlertRule.md)

[Add-AzureRmMetricAlertRule](./Add-AzureRmMetricAlertRule.md)

[Add-AzureRmWebtestAlertRule](./Add-AzureRmWebtestAlertRule.md)

[New-AzureRmAlertRuleWebhook](./New-AzureRmAlertRuleWebhook.md)


