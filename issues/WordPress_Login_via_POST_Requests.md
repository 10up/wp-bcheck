# WordPress Login via Crafted POST Requests with User Enumeration

## Issue detail

This vulnerability involves the acceptance of login attempts via crafted POST requests on a WordPress site, coupled with user enumeration. When an incorrect login attempt is made, WordPress may disclose whether the entered username exists, aiding attackers in user enumeration. Attackers can exploit this vulnerability to systematically guess usernames and passwords through brute force attacks, increasing the likelihood of gaining unauthorized access to user accounts and compromising sensitive information.

## Issue background

WordPress login functionality, by default, may reveal whether a login attempt failed due to an incorrect username or password. This behavior allows attackers to discern valid usernames by observing the response to failed login attempts. Armed with a list of valid usernames, attackers can then execute targeted brute force attacks to guess passwords associated with these usernames. Successful exploitation of this vulnerability can lead to unauthorized access to sensitive areas of the WordPress site, including the admin panel and user accounts, posing significant security risk.

## Issue remediation

Configure WordPress to display generic error messages for failed login attempts, refraining from disclosing whether the entered username or password was incorrect. By concealing this information, attackers are unable to ascertain the validity of usernames, thus diminishing the efficacy of user enumeration attacks.
Implement two-factor authentication (2FA) to provide an additional layer of security and deploy an account lockout and rate-limit mechanism that automatically locks user accounts for a designated period after a specified number of failed login attempts.

Additionally, consider disabling POST requests for wp-login to further fortify the site against potential login-related vulnerabilities. 

## Like what you see?

<p align="center">
<a href="http://10up.com/contact/"><img src="https://10up.com/uploads/2016/10/10up-Github-Banner.png" width="850"></a>
</p>
