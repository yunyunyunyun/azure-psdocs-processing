---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: D990961D-90EA-4969-BDC0-40B30B49E917
updated_at: 01/14/2017 00:01 AM
ms.date: 01/14/2017
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.ApiManagement/v2.1.0/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.ApiManagement/v2.1.0/Get-AzureRmApiManagementUser.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/da8eb594c0f0a447468b6e82a18c708dac6b5b28
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# Get-AzureRmApiManagementUser

## SYNOPSIS
Gets a user or users.

## SYNTAX

### Get all users (Default)
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### Get user by ID
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Find users
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureRmApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.

## EXAMPLES

### Example 1: Get all users
```
PS C:\> Get-AzureRmApiManagementUser -Context $ApiMContext
```

This command gets all users.

### Example 2: Get a user by ID
```
PS C:\> Get-AzureRmApiManagementUser -Context $ApiMContext -UserId "0123456789"
```

This command gets a user by ID.

### Example: Get users by last name
```
PS C:\> Get-AzureRmApiManagementUser -Context $ApiMContext -LastName "Fuller"
```

This command gets users that have a specified last name, Fuller.

### Example 4: Get a user by email address
```
PS C:\> Get-AzureRmApiManagementUser -Context $ApiMContext -Email 
"user@contoso.com"
```

This command gets the user that has the specified email address.

### Example 5: Get all users within a group
```
PS C:\> Get-AzureRmApiManagementUser -Context $ApiMContext -GroupId "0001"
```

This command gets all users within the specified group.

## PARAMETERS

### -Context
Specifies an instance of **PsApiManagementContext**.

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserId
Specifies a user ID.
If specified, this cmdlet finds the user by this identifier.
This parameter is optional.

```yaml
Type: String
Parameter Sets: Get user by ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FirstName
Specifies the first name of the user.
If this parameter is specified, this cmdlet finds a user by first name.
This parameter is optional.

```yaml
Type: String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LastName
Specifies the last name of a user.
If specified, this cmdlet finds users by last name.
This parameter is optional.

```yaml
Type: String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -State
Specifies the user state.
If specified, this cmdlet finds users in this state.
This parameter is optional.

```yaml
Type: PsApiManagementUserState
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Email
Specifies the email address of the user.
If this parameter is specified, this cmdlet finds a user by email.
This parameter is optional.

```yaml
Type: String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GroupId
Specifies the group identifier.
If specified, this cmdlet finds all users within the specified group.
This parameter is optional.

```yaml
Type: String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

## OUTPUTS

### IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser>

## NOTES

## RELATED LINKS

[New-AzureRmApiManagementUser](./New-AzureRmApiManagementUser.md)

[Remove-AzureRmApiManagementUser](./Remove-AzureRmApiManagementUser.md)

[Set-AzureRmApiManagementUser](./Set-AzureRmApiManagementUser.md)
