# OWASP: OWASP 10 2021










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
