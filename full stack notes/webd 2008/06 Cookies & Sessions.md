---
class: webd 2008
module: module three
date: 2022-02-09
tags: webd-2008, web-development, php, pdo, term-2
---

# Cookies & Sessions

### Cookies
- We can use cookies and sessions to transport data like the POST and GET
- When creating a cookie, we are saving information inside a user's browser
- It will not work cross-browser
- Inspector -> Storage -> Can view cookies and delete
- Can store username and password
- Cookies are stored on the computer

### Sessions

- Session variables are stored on the server so users cannot see
- This is good for perhaps purchasing
- Session goes until browser close

#### session_start();
- Always start with this in the php block
- User does not have access to the value but can delete the session cookie