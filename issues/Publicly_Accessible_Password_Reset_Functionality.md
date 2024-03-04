# Publicly Accessible Password Reset Functionality

## Issue detail

One of the endpoints "/wp-login.php?action=rp", "/wp-login.php?action=resetpass", "/wp-login.php?action=lostpassword", and "/wp-login.php?action=lostpassword&error=invalidkey" are publicly available, allowing anyone to initiate password reset requests for user accounts. Additionally, WordPress may inadvertently disclose whether a username exists during the password reset process, which can aid attackers in identifying valid user accounts.

## Issue background

WordPress provides a password reset mechanism that allows users to request a password reset link via email when they forget their password. However, if the password reset functionality is publicly accessible, it can be exploited by attackers to target specific user accounts. By initiating password reset requests for known or guessed usernames, attackers can determine whether a username is valid based on the response from WordPress. This information disclosure can aid attackers in launching targeted attacks against valid user accounts, increasing the risk of unauthorized access and potential security breaches. Additionally, vulnerabilities in the password reset process, such as insufficient validation or insecure email transmission, can further exacerbate the security risks associated with this issue.

## Issue remediation

If disabling the password reset functionality on the wp-login.php area is not feasible, alternative measures should be considered. Adjust WordPress settings or customize error messages to prevent the disclosure of whether a username exists during the password reset process. Implement supplementary verification measures, such as multi-factor authentication or security questions, to validate the user's identity before permitting password resets. 

## Like what you see?

<p align="center">
<a href="http://10up.com/contact/"><img src="https://10up.com/uploads/2016/10/10up-Github-Banner.png" width="850"></a>
</p>
