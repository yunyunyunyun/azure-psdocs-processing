---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 5B5D5CC5-633F-431D-AFB9-A59C17420608
updated_at: 01/09/2017 23:01 PM
ms.date: 01/09/2017
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Resources/v3.1.0/Get-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Resources/v3.1.0/Get-AzureRmResourceGroup.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/909020b7dbd03ec23a61b4fe16ccd2762277084c
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# Get-AzureRmResourceGroup

## SYNOPSIS
Gets resource groups.

## SYNTAX

### Lists the resource group based on the name. (Default)
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [<CommonParameters>]
```

### Lists the resource group based on the Id.
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureRmResourceGroup** cmdlet gets Azure resource groups in the current subscription.
You can get all resource groups, or specify a resource group by name or by other properties.
By default, this cmdlet gets all resource groups in the current subscription.

For more information about Azure resources and Azure resource groups, see the **New-AzureRmResourceGroup** cmdlet.

## EXAMPLES

### Example 1: Get a resource group by name
```
PS C:\> Get-AzureRmResourceGroup -Name "EngineerBlog"
```

This command gets the Azure resource group in your subscription named EngineerBlog.

### Example 2: Get all tags of a resource group
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

This command gets the resource group named ContosoRG, and displays the tags associated with that group.

## PARAMETERS

### -Id
Specifies the ID of the resource group to get.
Wildcard characters are not permitted.

```yaml
Type: String
Parameter Sets: Lists the resource group based on the Id.
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location
Specifies the location of the resource group to get.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApiVersion
Specifies the API version that is supported by the resource Provider.
You can specify a different version than the default version.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of the resource group to get.
Wildcard characters are not permitted.

```yaml
Type: String
Parameter Sets: Lists the resource group based on the name.
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### String
You can pipe input to the cmdlet by property name, but not by value.

## OUTPUTS

### Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup
This cmdlet returns resource groups.

## NOTES

## RELATED LINKS

[New-AzureRmResourceGroup](./New-AzureRmResourceGroup.md)

[Remove-AzureRmResourceGroup](./Remove-AzureRmResourceGroup.md)

[Set-AzureRmResourceGroup](./Set-AzureRmResourceGroup.md)


