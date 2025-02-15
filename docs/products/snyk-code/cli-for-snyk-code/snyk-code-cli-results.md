# Understanding the Snyk Code CLI results

After you run the `snyk code test` command in the CLI, the results of the Snyk Code test are presented in the terminal in one block that includes 3 sections:

![](<../../../.gitbook/assets/Snyk Code - CLI - snyk code test - Results Details.png>)

**Note**: The **Ignore** issue option is not applicable to the CLI test results. If you ignored issues on the Snyk Web UI, these issues would still appear in the CLI results.

### The list of vulnerability issues detected by Snyk Code

The list of issues discovered in the Snyk Code test is organized by the severity level of the issues, from low to high.

For each detected issue, the following information is provided:

![](<../../../.gitbook/assets/Snyk Code - CLI - snyk code test - Results - Issue Details.png>)

* Header: The severity level and vulnerability type of the issue.
* **Path:** The file name and the line in the file where the issue was found. These location details refer to the Sink of the issue, meaning where the vulnerability may be executed in the tested repository.
* **Info**: A description of the data flow of the issue.

**Note:** The message that appears in the **Info** section is the same as the one in the **Data flow** section on the Web UI:

![](<../../../.gitbook/assets/Snyk Code - CLI - snyk code test - Results - Issue Details - in the Web UI.png>)

### General info about the test

The general info about the test results includes the following details:

![](<../../../.gitbook/assets/Snyk Code - CLI - snyk code test - Results - General test info.png>)

* Test success: Whether the test was completed or not.
* **Organization:** The Snyk ID or internal name of the organization under which the test run. For more information, see [Before you start – Set the organization for the CLI tests](before-you-start-set-the-organization-for-the-cli-tests/).
* **Test type:** The type of test command that generated the results. For Snyk Code, it is always “**Static code analysis**”.
* **Project path:** The path of the tested repository.&#x20;

### Summary of the test findings

The summary of the test findings includes the following details:

![](<../../../.gitbook/assets/Snyk Code - CLI - snyk code test - Results - Test summary.png>)

* The number of vulnerability issues that were discovered by Snyk Code in the tested repository.
* The number of discovered issues per severity level.

&#x20;

### The Exit Codes of the test results

The `snyk code test` command ends with one of the following exit codes:

**0**: Success, no vulnerabilities were found.

**1**: Action needed, vulnerabilities were found.

**2**: Failure, try to re-run the command.

**3**: Failure, no supported files were found.

