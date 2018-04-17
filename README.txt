#Randy Santiago
#
# Project 8 - Pentesting Live Targets

Time spent: **15** hours spent in total

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

Vulnerability #1: Session Hijacking
                    grabbing one session ID anf input it into another from the url you have provided. Only issue was thinking the result was immediate but i had to login and it was done
                Screenshot: Sess 1 and 2 png

Vulnerability #2: SQLI
                    The tricky part was trying to find where to put the SQLI where it needs to go. Then i realize the id of the salespeople on the url was the answer
                Screenshot: SQLI 1, 2, and 3 png


## Green

Vulnerability #1: Store Cross-Site Scripting
                putting <script>alert('Mallory found the XSS!');</script> in the feedback section and making sure it works by loggining in.
                ScreenShot: XXS.png

Vulnerability #2: Username Enumeration
                The log in was unsuccessful was bold if the username existed if it didn't then it was not bolded
                User 1 & User 2 .png

## Red

Vulnerability #1: IDOR
                    they left id open instead of blacklisting them like the rest. The rest sends the guest to the main salesperson page
                    ScreenShot: IDOR.png

Vulnerability #2: CSRF
                    The issue was going back to Green to do a stored XSS in order to manipulate it then figuring out which URL to attack.
                    ScreenShot: CSRF 1 and 2 png


## Notes

Describe any challenges encountered while doing the work