---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: BC38484D-C0CF-49FC-B300-3AE62F8D8832
updated_at: 11/01/2016 22:11 PM
ms.date: 11/01/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Network/v1.0.13/Stop-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Network/v1.0.13/Stop-AzureRmApplicationGateway.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/f59f3ef60bc592383812213e69fd77ba950759ed
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# Stop-AzureRmApplicationGateway

## SYNOPSIS
Stops an application gateway

## SYNTAX

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Stop-AzureRmApplicationGateway** cmdlet stops an application gateway.

## EXAMPLES

### Example 1: Stop an application gateway
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

This command stops the application gateway stored in the $AppGw variable.

## PARAMETERS

### -ApplicationGateway
Specifies the application gateway that this cmdlet stops.

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InformationAction
Specifies how this cmdlet responds to an information event.

The acceptable values for this parameter are:

- Continue
- Ignore
- Inquire
- SilentlyContinue
- Stop
- Suspend

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Specifies an information variable.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureRmApplicationGateway](./Get-AzureRmApplicationGateway.md)

[New-AzureRmApplicationGateway](./New-AzureRmApplicationGateway.md)

[Remove-AzureRmApplicationGateway](./Remove-AzureRmApplicationGateway.md)

[Set-AzureRmApplicationGateway](./Set-AzureRmApplicationGateway.md)

[Start-AzureRmApplicationGateway](./Start-AzureRmApplicationGateway.md)


