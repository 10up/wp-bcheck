# User Enumeration via REST API

## Issue detail

An attacker can gather information about valid usernames registered on the WordPress site via the REST API endpoint, which can potentially aid in further attacks such as brute force attacks or targeted phishing attempts.

## Issue background

WordPress provides a REST API that allows developers to interact with WordPress sites programmatically. However, certain endpoints, such as /wp-json/wp/v2/users, can inadvertently expose sensitive information like user data if not properly secured. This vulnerability can be exploited by malicious actors to enumerate valid usernames on the WordPress site, which is often the first step in launching more sophisticated attacks against the site or its users.

## Issue remediation

 Limit access to the /wp-json/wp/v2/users endpoint to authenticated users only or restrict it entirely if it's not necessary for functionality. Furthermore, apply rate limiting mechanisms to prevent excessive requests to the REST API, which can mitigate automated user enumeration attempts.

## Like what you see?

<p align="center">
<a href="http://10up.com/contact/"><img src="https://10up.com/uploads/2016/10/10up-Github-Banner.png" width="850"></a>
</p>
