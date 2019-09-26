---
note: generated by cobra
path: /cmd/docs.go
---
# kabanero CLI
## kabanero

This repo defines a command line interface used by the enterprise, solution, or application architect who defines and manages the kabanero collections that are used by developers to create governed applications for their business.

### Synopsis

**kabanero** is a command line interface for managing the collections in a Kabanero 
environment, as well as to on-board the people that will use 
the environment to build applications.

Complete documentation is available at https://kabanero.io

### Options

```
  -h, --help      help for kabanero
  -v, --verbose   Turns on debug output and logging to a file in $HOME/.kabanero/logs
```

### SEE ALSO

* [kabanero deactivate](#kabanero-deactivate)	 - Remove the specified collection from the list of available application types, without deleting it from the Kabanero instance.
* [kabanero list](#kabanero-list)	 - List all the collections in the kabanero instance, and their status
* [kabanero login](#kabanero-login)	 - Will authenticate you to a Kabanero instance
* [kabanero logout](#kabanero-logout)	 - Disconnect from Kabanero instance
* [kabanero onboard](#kabanero-onboard)	 - Command to onboard a developer to the Kabanero infrastructure
* [kabanero refresh](#kabanero-refresh)	 - Refresh the collections list
* [kabanero version](#kabanero-version)	 - Show Kabanero CLI version

###### Auto generated by spf13/cobra on 26-Sep-2019
## kabanero login

Will authenticate you to a Kabanero instance

### Synopsis


	Login to a Kabanero instance using Github credentials, and store a temporary access token for subsequent command line calls.
	The temporary authentication token will be stored in your-home-directory/.kabanero/config.yaml.
	Use your Github userid and either password or Personal Access Token (PAT).
	

```
kabanero login kabanero-url -u Github userid -p Github-PAT|Github-password  [flags]
```

### Examples

```

	# login with Github userid and password:
	kabanero login my.kabaneroInstance.io -u myGithubID -p myGithubPassword

	# login with previously used url Github userid and PAT:
	kabanero login -u myGithubID -p myGithubPAT
	
```

### Options

```
  -h, --help              help for login
  -p, --password string   github password/PAT
  -u, --username string   github username
```

### Options inherited from parent commands

```
  -v, --verbose   Turns on debug output and logging to a file in $HOME/.kabanero/logs
```

### SEE ALSO

* [kabanero](#kabanero)	 - This repo defines a command line interface used by the enterprise, solution, or application architect who defines and manages the kabanero collections that are used by developers to create governed applications for their business.

###### Auto generated by spf13/cobra on 26-Sep-2019
## kabanero logout

Disconnect from Kabanero instance

### Synopsis


Disconnect from the instance of Kabanero that you 
have been interacting with.

```
kabanero logout [flags]
```

### Options

```
  -h, --help   help for logout
```

### Options inherited from parent commands

```
  -v, --verbose   Turns on debug output and logging to a file in $HOME/.kabanero/logs
```

### SEE ALSO

* [kabanero](#kabanero)	 - This repo defines a command line interface used by the enterprise, solution, or application architect who defines and manages the kabanero collections that are used by developers to create governed applications for their business.

###### Auto generated by spf13/cobra on 26-Sep-2019
## kabanero list

List all the collections in the kabanero instance, and their status

### Synopsis

List all the collections in the kabanero instance, and their status

```
kabanero list  [flags]
```

### Options

```
  -h, --help   help for list
```

### Options inherited from parent commands

```
  -v, --verbose   Turns on debug output and logging to a file in $HOME/.kabanero/logs
```

### SEE ALSO

* [kabanero](#kabanero)	 - This repo defines a command line interface used by the enterprise, solution, or application architect who defines and manages the kabanero collections that are used by developers to create governed applications for their business.

###### Auto generated by spf13/cobra on 26-Sep-2019
## kabanero refresh

Refresh the collections list

### Synopsis

Run the kabanero refresh command to refresh the list of collections from master, making these collections current with the activated collections across all namespaces in the Kabanero instance. This command can also be used to restore deactivated collections. See kabanero deactivate.

```
kabanero refresh [flags]
```

### Options

```
  -h, --help   help for refresh
```

### Options inherited from parent commands

```
  -v, --verbose   Turns on debug output and logging to a file in $HOME/.kabanero/logs
```

### SEE ALSO

* [kabanero](#kabanero)	 - This repo defines a command line interface used by the enterprise, solution, or application architect who defines and manages the kabanero collections that are used by developers to create governed applications for their business.

###### Auto generated by spf13/cobra on 26-Sep-2019
## kabanero onboard

Command to onboard a developer to the Kabanero infrastructure

### Synopsis

Under development.  In the future this command causes an email to be sent to the user associated
	with the user-id providing the information necessary to get started using 
	Kabanero.

```
kabanero onboard github-id repo-url|org-url [flags]
```

### Options

```
  -h, --help   help for onboard
```

### Options inherited from parent commands

```
  -v, --verbose   Turns on debug output and logging to a file in $HOME/.kabanero/logs
```

### SEE ALSO

* [kabanero](#kabanero)	 - This repo defines a command line interface used by the enterprise, solution, or application architect who defines and manages the kabanero collections that are used by developers to create governed applications for their business.

###### Auto generated by spf13/cobra on 26-Sep-2019
## kabanero deactivate

Remove the specified collection from the list of available application types, without deleting it from the Kabanero instance.

### Synopsis


Run the deactivate command to remove the specified collection from the list of available application types, without deleting it from the Kabanero instance.

This command is useful in a case where you have cloned a collection and customized it for your business needs. Deactivation keeps the base collection in the app hub. The base collection continues to be updated and the updates percolate up to your cloned collection. To restore a deactivated collection, run the kabanero refresh command.

```
kabanero deactivate collection-name [flags]
```

### Options

```
  -h, --help   help for deactivate
```

### Options inherited from parent commands

```
  -v, --verbose   Turns on debug output and logging to a file in $HOME/.kabanero/logs
```

### SEE ALSO

* [kabanero](#kabanero)	 - This repo defines a command line interface used by the enterprise, solution, or application architect who defines and manages the kabanero collections that are used by developers to create governed applications for their business.

###### Auto generated by spf13/cobra on 26-Sep-2019
