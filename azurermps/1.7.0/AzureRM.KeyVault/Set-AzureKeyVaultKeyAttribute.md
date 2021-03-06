---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: C23E766E-ED96-4AAD-A0CD-62625AA91F4C
updated_at: 11/11/2016 23:11 PM
ms.date: 11/11/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.KeyVault/v1.1.11/Set-AzureKeyVaultKeyAttribute.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.KeyVault/v1.1.11/Set-AzureKeyVaultKeyAttribute.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/79eeb985ea480979357fb4695832a0c3d29a48bf
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# Set-AzureKeyVaultKeyAttribute

## SYNOPSIS
Updates the attributes of a key in a key vault.

## SYNTAX

```
Set-AzureKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tags <Hashtable>] [-PassThru]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-AzureKeyVaultKeyAttribute** cmdlet updates the editable attributes of a key in a key vault.

## EXAMPLES

### Example 1: Modify a key to enable it, and set the expiration date and tags
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime() 
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tags $Tags -PassThru
```

The first command creates a **DateTime** object by using the **Get-Date** cmdlet.
That object specifies a time two years in the future.
The command stores that date in the $Expires variable.
For more information, type `Get-Help Get-Date`.

The second command creates a variable to store tag values of high severity and Accounting.

The final command modifies a key named ITSoftware.
The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.

### Example 2: Modify a key to delete all tags
```
PS C:\>Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tags @{}
```

This commands deletes all tags for a specific version of a key named ITSoftware.

## PARAMETERS

### -Enable
Specifies whether to enable or disable a key.
A value of $True enables the key.
A value of $False disables the key.
If you do not specify this parameter, this cmdlet does not modify the status of the key.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Expires
Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet updates.
This parameter uses Coordinated Universal Time (UTC).
To obtain a **DateTime** object, use the **Get-Date** cmdlet.
For more information, type `Get-Help Get-Date`.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -KeyOps
Specifies an array of operations that can be performed by using the key that this cmdlet adds.
If you do not specify this parameter, all operations can be performed.

The acceptable values for this parameter are a comma-separated list of key operations as defined by the JSON Web Key specification.
These values (case-sensitive) are: 

- encrypt 
- decrypt 
- wrap 
- unwrap 
- sign 
- verify
- backup
- restore

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Specifies the name of the key to update.
This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotBefore
Specifies the time, as a **DateTime** object, before which the key cannot be used.
This parameter uses UTC.
To obtain a **DateTime** object, use the **Get-Date** cmdlet.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
passthru

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

### -Tags
Specifies a hash table that represents tags for a secret. If you do not specify this parameter, there is no change to the current secret's tags. To remove a tag, specify an empty hash table. For more information about resource tags, see Using tags to organize your Azure resources (http://go.microsoft.com/fwlink/?LinkId=613624).

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Specifies the name of the key vault in which this cmdlet modifies the key.
This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Specifies the key version.
This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### String, Boolean, DateTime

## OUTPUTS

### Microsoft.Azure.Commands.KeyVault.Models.KeyBundle

## NOTES

## RELATED LINKS

[Add-AzureKeyVaultKey](./Add-AzureKeyVaultKey.md)

[Get-AzureKeyVaultKey](./Get-AzureKeyVaultKey.md)

[Remove-AzureKeyVaultKey](./Remove-AzureKeyVaultKey.md)


