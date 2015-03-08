# Test-EmailAddress
PowerShell function intended to verifying the correctness of addresses email in Microsoft Exchange environment.

Function which can be used to verifying an email address before for example adding it to Microsoft Exchange environment as next email/proxy address. 

##Checks performed
* if an email address contains wrong characters e.g. % or spaces
* if an email address is from domain which are on accepted domains list
* if an email address is currently assigned to any object in Exchange environment
* if an email address contains white chars e.g. spaces or tabs at the beginning or at the end

##Results

As the result returned is PowerShell object which contain: EmailAddress, ExitCode, ExitDescription, ConflictedObjectAlias, ConflictedObjectType.
		
###Exit codes and descriptions
* 0 - No Error
* 1 - Email doesn't contain 'at' char
* 2 - Email exist now
* 3 - Unsupported chars found
* 4 - Not accepted domain
* 5 - White chars e.g. spaces founded before/after email
