# OWASP: OWASP 10 2021

### A05 Security Misconfiguration

From :[A05 Security Misconfiguration](https://owasp.org/Top10/A05_2021-Security_Misconfiguration/)

Here there are listed reasons why an application might be vulnerable such as:

- Security hardening is missing across any part of the application stack
- Cloud Service permissions are improperly configured
- Uneccessary features are enabled

Systems are at higher risk without a repeatable application security configuration process.

Ways to prevent:

- Implement secure installation processes
- Use a repeatable hardening process for identical configuration in development
- Deploy a minimal platform without unnecessary features or components
- Review and update regurarly the configurations
- Implement a segmented application architecture for secure separation between components or tenants
- Use securit headers and automate the verification of configurations in all environments

Attack scenarios:

- Cloud service provider's default sharing permissions expose sensitive data stored within cloud storage to other users on the internet
- Directory listing not disable on the server, which allows an attacker to access and exploit a flaw in the application
- Application server configuration allows detailed error messages, exposing sensitive information
- Sample application with security flaws left on the production server, which allows an attacker to compromise the server by exploiting default accounts and passwords


### A06 Vulnerable and Outdated Components

From: [A06 Vulnerable and Outdated Components](https://owasp.org/Top10/A06_2021-Vulnerable_and_Outdated_Components/)

Vulnerable components category is difficult to test and assess risk.

Vulnerability can arise from:

- Being unaware of all components, including direct and nested dependencies
- Software is outdated or unsupported
- Lack of regural vulnerability scans and subscription to security bulletins
- Failure to fix or upgrade underlying platforms, frameworks and dependencies in a timely fashion
- Lack of compatibility testing for updated, upgraded or patched libraries
- Inadequate seecuriy for components' configurations

Ways to prevent issues:

- Remove unused dependencies, unnecessary features, components, files and documentation
- Obtain components only from official sources over secure links
- Prefer signed packages to reduce the risk of including modified, malicious components
- Monitor and address issues with unmaintained or insecure components
- Use software composition analysis tools and subscribe to alerts for security vulnerabilities
- Monitor Common Vulnerabilities and Exposures (CVE) and National Vulnerability Database (NVD) usage

Attack scenarios:
Components running with the same priviliges as the applicatioin result in serious impact flaws:

- A Struts 2 remote code execution vulnerability
- IoT devices can have critical vulnerabilties
- Automated tools like Shodan IoT search engine used to find unpatched or misconfigured systems (Heartbleed vulnerability)


### A03 Injection

94% of applications tested for injection had a max incidence rate of 19%, average incident rate of 3% and 274k occurrences.

An application becomes susceptible to attacks under the following conditions:

- The application fails to validate, filter, or sanitize user-supplied data
- Dynamic queries or non-parameterized calls are utilized in the interpreter without context-aware escaping
- Object-relational mapping (ORM) search parameters incorporate hostile data, leading to the extraction of additional sensitive records
- Malicious data is either directly used or concatenated in dynamic queries, commands, or stored procedures, compromising the structure of SQL or command and posing a security threat

To prevent injection, it is crucial to maintain a separation between data and commands/queries. The recommended approaches include:

- Utilize a secure API
- Implement positive server-side input validation
- For any remaining dynamic queries, employ escape syntax
- Incorporate SQL controls such as LIMIT

Attack scenarios:

- Application constructs a vulnerable SQL call.

'''String query = "SELECT * FROM accounts WHERE custID='" + request.getParameter("id") + "'";'''

Attacker can modify the 'id' parameter to execute unauthorized actions.


## Webgoat 2023.4: General: Developer tools

![First Step](https://github.com/PanosArvan/Information-Security/assets/145275148/88d2b9d3-2cf0-44e3-b841-edd9823edc78)

First I pasted the Javascript code, that then gave me a number, which I pasted in the box.

![Second Step](https://github.com/PanosArvan/Information-Security/assets/145275148/b6968d8f-d02c-4241-a900-05ded1f3c9d5)

Task 4 solved.

![First Step2](https://github.com/PanosArvan/Information-Security/assets/145275148/60d3327b-fb3e-4e97-a719-0657089822a1)

Pressed GO. From that I got in the networks tab in developer tools a file called 'network'.

![Second Step2](https://github.com/PanosArvan/Information-Security/assets/145275148/f0395ca1-c3e2-4972-a35a-a2d98dfff4f3)

In the Request page I found the networkSum number, which I pasted to the submit box.

Task 6 solved.

## SQLZoo

### 0 SELECT Basics

![First](https://github.com/PanosArvan/Information-Security/assets/145275148/85551170-7475-4e7f-8261-df7314494bff)

For the this excersice I changed 'France' to 'Germany' and got the correct answer.

### 2 SELECT WORLD

### Subtask 1

![First](https://github.com/PanosArvan/Information-Security/assets/145275148/f01d1bb7-7ecf-41d8-8537-9c8082b07aff)

Just running the SQL gives us the answer, which is a table with countries and information about them.

### Subtask 2

![First](https://github.com/PanosArvan/Information-Security/assets/145275148/ea4c0aa1-3f75-4ebe-ab0b-09d2b24d988c)

Changed the SQL code to --> WHERE population>=20000000 and it gave the correct answer within a table.

## Portswigger Lab: SQL injection vunlerability in WHERE clause

![ninth](https://github.com/PanosArvan/Information-Security/assets/145275148/fbcfa913-fd00-4ed3-9169-9646065ae794)

First went to Access Lab.

![tenth](https://github.com/PanosArvan/Information-Security/assets/145275148/5a26dba3-1a84-498e-9436-793277b98bd0)

Then I was greeted by this page.

![eleventh](https://github.com/PanosArvan/Information-Security/assets/145275148/16e648e4-a4f8-4d8e-8de3-5d08c4d08f1a)

I chose first 'tech gifts' to enable SQL search.

![twelfth](https://github.com/PanosArvan/Information-Security/assets/145275148/34ac9c3f-4fa1-4b2e-8d81-f212c4f08617)

Then I inputted "'+OR+1=1--" that allowed me to see other hidden elements within that page that were not initially meant to be seen.

The modified query returns all items where either the category is tech gifts, or 1 is equal to 1. As 1=1 is always true, the query returns all items.
The -- removes anything else the page tries to do.
