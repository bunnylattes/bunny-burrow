---
class: webd 2008
module: module two
date: 2022-01-19
tags: webd-2008, web-development, php, validation, sanitization, term-2
---
# Input Validation Sanitization

Class: WEBD-2008
Created: January 19, 2022 3:57 PM
Module: Module 2
Reviewed: No

**Superglobals**

- Predefined variables in PHP that are always accessible, regardless of scope, and you can access them from any function, class, or file.
- 9 PHP superglobals

**GET**

- $_GET can be used to collect form data after submitting an HTML form with method=”get” in the form tag
- collects data via URL
    - < ahref=”text_get.php?subject=PHP&web=W3schools.com”>
    - parameters are subject and web

**POST**

- $_POST is used to collect data as well as pass variables using method=”post” in the form tag
- data is passed using the HTTP headers, rather than the URL that the GET uses, it’s more “behind the scenes”

**<pre></pre>**

- pre tag puts it on its own line, like a semi-block
- <pre><?php print_r($_GET) ?></pre>

**q**

- parameter which means query
- common in search engines

**Forms**

- the name attribute is what creates the keys when the data is sent to the server
- must consider sanitization

**Input Validation & Sanitization**

- user input could end up in our database tables or markup
- we must have it match our expectations so the website remains stable and secure
- **Validation**: checking foreign input (we have done with javascript)
- **Sanitizing**: cleaning foreign input
- NEVER TRUST FOREIGN DATA

**Foreign Input Sources**

- $_GET, $_POST, $_SERVER
- Session / Cookie Values
- Uploaded Files
- 3rd Party API Requests
- Internal Data Integration Systems

**filter_input**

- filter_input(INPUT_POST, ‘user_age’, FILTER_VALIDATE_INT);
- takes three parameters: the type of input, the input, and then the type of filter
- for example, FILTER_SANITIZE_FULL_SPECIAL_CHARS can eliminate malicious code by taking the special characters such as < and >, it removes the special characters and replaces it with their text representation
    - < becomes &lt;
- consider apostrophes in names etc

**When testing assignment, turn off javascript**

- about:config
    - javascript.enabled (change to off)

***Data security needs php validation, Javascript is for user experience.***