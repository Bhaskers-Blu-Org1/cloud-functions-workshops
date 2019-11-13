# Setting Up the CLI

This section will take you step-by-step through [Getting started with the IBM Cloud CLI and Developer Tools](https://cloud.ibm.com/docs/cli?topic=cloud-cli-getting-started) using the command line option.

### Install IBM Cloud CLI [🔗](https://cloud.ibm.com/docs/cli?topic=cloud-cli-getting-started#step1-install-idt)

Download the `ibmcloud` CLI by running the command appropriate for your operating system:

- **MacOS & Linux**:
    ```bash
    $ curl -sL https://ibm.biz/idt-installer | bash
    ```
- **Windows 10 Pro** (Powershell)
Run the following as Administrator:
    ```bash
    $ [Net.ServicePointManager]::SecurityProtocol = "Tls12"; iex(New-Object Net.WebClient).DownloadString('https://ibm.biz/idt-win-installer')
    ```
     - _**Tip** Right-click the Windows™ PowerShell icon, and select Run as administrator._

### Verify the Installation [🔗](https://cloud.ibm.com/docs/cli?topic=cloud-cli-getting-started#step2-verify-idt)

Try running the help command:
```bash
$ ibmcloud dev help
```

### Login and Configure the IBM Cloud CLI [🔗](https://cloud.ibm.com/docs/cli?topic=cloud-cli-getting-started#step3-configure-idt-env)

1. Use this command to authenticate the IBM Cloud CLI with your account credentials.

   ```bash
   $ ibmcloud login
   ```

1. Enter account credentials for your IBM Cloud account.

    ```bash
    Email> josephine.watson@gmail.com

    Password>
    Authenticating...
    OK

    Targeted account Josephine Watson's Account (87a302ad58884640a45f959d3da6cc77)


    API endpoint:      https://cloud.ibm.com
    Region:            us-south
    User:              josephine.watson@gmail.com
    Account:           Josephine Watson's Account (87a302ad58884640a45f959d3da6cc77)
    Resource group:    No resource group targeted, use 'ibmcloud target -g RESOURCE_GROUP'
    CF API endpoint:
    Org:
    Space:
    ```

    _Note: If you already have created an IBM Cloud account you may be prompted to select the account you wish the IBM Cloud CLI to use:_

    ```bash
    Select an account (or press enter to skip):
    Select an account:
    1. Josephine Watson's Account (87a302ad58884640a45f959d3da6cc77)

    Enter a number> 1
    ```

1. Configure your Cloud Foundry organization and space the CLI is targeting.

    Run the following interactive command:
    ```bash
    $ ibmcloud target --cf
    ```

    ```bash
    Targeted Cloud Foundry (https://api.ng.bluemix.net)
    Targeted org josephine.watson@gmail.com
    Targeted space dev

    API endpoint:      https://cloud.ibm.com
    Region:            us-south
    User:              josephine.watson@gmail.com
    Account:           Josephine Watson's Account (87a302ad58884640a45f959d3da6cc77)
    Resource group:    No resource group targeted, use 'ibmcloud target -g RESOURCE_GROUP'
    CF API endpoint:   https://api.ng.bluemix.net (API version: 2.142.0)
    Org:               ljosephine.watson@gmail.com
    Space:             dev
    ```
---
🎉 **Congratulations, you've successfully registered an IBM Cloud account and logged into the IBM Cloud CLI.** 🎉
