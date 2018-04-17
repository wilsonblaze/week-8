# Project 8 - Pentesting Live Targets

Time spent: **X** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: SQLi 
Daron Burke salesperson allows SQLi for delay. I posted 'OR SLEEP(5)=0-- ' into the end of the url.

Vulnerability #2: Session Hijacking/Fixation
posted "public/hacktools/change_session_id.php" into the url of a logged in browser. Took the session id and changed the session id of a non-logged in browser.


## Green

Vulnerability #1: Username Enumeration
non-existing usernames will prompt a non-bold "Log in was unsuccessful"

Vulnerability #2: XSS
input XSS <script>alert('Mallory found the XSS!');</script> into comment section and logged in and clicked feedback.


## Red

Vulnerability #1: IDOR
change id to 10 for a hidden salesperson.

Vulnerability #2: CSRF
Input the following into the comment section. Clicking on feedback brings you to the following new state.
<form action="https://35.226.125.219/red/public/staff/states/show.php?id=32" method="POST">
<input type="hidden" name="name" value="MARIA"/>
<input type="hidden" name="amount" value="100000"/>
<input type="submit" value="View my pictures"/>
</form>

## Notes

Describe any challenges encountered while doing the work
