---
note: generated by cobra
path: /cmd/docs.go
---
# kabanero CLI
## kabanero

This repo defines a command line interface used by the enterprise, solution, or application architect who defines and manages the kabanero stacks that are used by developers to create governed applications for their business.

### Synopsis

**kabanero** is a command line interface for managing the stacks in a Kabanero 
environment, as well as to on-board the people that will use 
the environment to build applications.

Before using the cli please configure the github authorization for the cli service. Steps can be found in the following documentation: https://kabanero.io/docs/ref/general/github-authorization.html


Complete documentation is available at https://kabanero.io

### Options

```
  -h, --help      help for kabanero
  -v, --verbose   Turns on debug output and logging to a file in $HOME/.kabanero/logs
```

### SEE ALSO

* [kabanero deactivate](#kabanero-deactivate)	 - Remove the specified stack from the list of available application types, without deleting it from the Kabanero instance.
* [kabanero list](#kabanero-list)	 - List all the stacks in the kabanero instance, and their status
* [kabanero login](#kabanero-login)	 - Will authenticate you to a Kabanero instance
* [kabanero logout](#kabanero-logout)	 - Disconnect from Kabanero instance
* [kabanero onboard](#kabanero-onboard)	 - Command to onboard a developer to the Kabanero infrastructure
* [kabanero sync](#kabanero-sync)	 - sync the stack list
* [kabanero version](#kabanero-version)	 - Show Kabanero CLI version

###### Auto generated by spf13/cobra on 7-Feb-2020
## kabanero login

Will authenticate you to a Kabanero instance

### Synopsis


	Logs in to a Kabanero instance using Github credentials, and stores a temporary access token for subsequent command line calls.
	The temporary authentication token will be stored in your-home-directory/.kabanero/config.yaml.
	Use your Github userid and either password or Personal Access Token (PAT).
	* If you use a GitHub Personal Access Token, make sure it has **read:org** scope. You can select this when creating your PAT in GitHub
	

```
kabanero login kabanero-url -u Github userid /n PASSWORDPROMPT:GitHub Password|PAT [flags]
```

### Examples

```

	# login with Github userid and password:
	kabanero login my.kabaneroInstance.io -u myGithubID 
	# login with previously used url Github userid and PAT:
	kabanero login -u myGithubID 
	
```

### Options

```
  -h, --help              help for login
  -u, --username string   github username
```

### Options inherited from parent commands

```
  -v, --verbose   Turns on debug output and logging to a file in $HOME/.kabanero/logs
```

### SEE ALSO

* [kabanero](#kabanero)	 - This repo defines a command line interface used by the enterprise, solution, or application architect who defines and manages the kabanero stacks that are used by developers to create governed applications for their business.

###### Auto generated by spf13/cobra on 7-Feb-2020
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

* [kabanero](#kabanero)	 - This repo defines a command line interface used by the enterprise, solution, or application architect who defines and manages the kabanero stacks that are used by developers to create governed applications for their business.

###### Auto generated by spf13/cobra on 7-Feb-2020
## kabanero list

List all the stacks in the kabanero instance, and their status

### Synopsis

List all the stacks in the kabanero instance, and their status. 
	Modifications to the curated stack may be slow to replicate in git hub and therefore may not be reflected immediately in KABANERO LIST or SYNC display output

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

* [kabanero](#kabanero)	 - This repo defines a command line interface used by the enterprise, solution, or application architect who defines and manages the kabanero stacks that are used by developers to create governed applications for their business.

###### Auto generated by spf13/cobra on 7-Feb-2020
## kabanero sync

sync the stack list

### Synopsis

Run the kabanero sync command to synchronize the list of kabanero instance stacks with the curated stacks from github. This will activate/deactivate as well as update versions of the kabanero stacks to reflect the state of the curated stacks.
	See also kabanero deactivate.
	Modifications to the curated stacks may be slow to replicate in git hub and therefore may not be reflected immediately in KABANERO LIST or SYNC display output
	

```
kabanero sync [flags]
```

### Options

```
  -h, --help   help for sync
```

### Options inherited from parent commands

```
  -v, --verbose   Turns on debug output and logging to a file in $HOME/.kabanero/logs
```

### SEE ALSO

* [kabanero](#kabanero)	 - This repo defines a command line interface used by the enterprise, solution, or application architect who defines and manages the kabanero stacks that are used by developers to create governed applications for their business.

###### Auto generated by spf13/cobra on 7-Feb-2020
## kabanero onboard

Command to onboard a developer to the Kabanero infrastructure

### Synopsis

Under development.  In the future this command causes an email to be sent to the user associated
	with the user-id providing the information necessary to get started using 
	Kabanero.

```
kabanero onboard github-id [flags]
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

* [kabanero](#kabanero)	 - This repo defines a command line interface used by the enterprise, solution, or application architect who defines and manages the kabanero stacks that are used by developers to create governed applications for their business.

###### Auto generated by spf13/cobra on 7-Feb-2020
## kabanero deactivate

Remove the specified stack from the list of available application types, without deleting it from the Kabanero instance.

### Synopsis


Run the deactivate command to remove the specified stack from the list of available application types, without deleting it from the Kabanero instance.

This command is useful in a case where you have cloned a stack and customized it for your business needs. Deactivation keeps the base stack in the app hub. The base stack continues to be updated and the updates percolate up to your cloned stack. To restore a deactivated stack, run the kabanero refresh command.

```
kabanero deactivate stack-name version [flags]
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

* [kabanero](#kabanero)	 - This repo defines a command line interface used by the enterprise, solution, or application architect who defines and manages the kabanero stacks that are used by developers to create governed applications for their business.

###### Auto generated by spf13/cobra on 7-Feb-2020
