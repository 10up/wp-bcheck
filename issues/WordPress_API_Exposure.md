# WordPress API Exposure

## Issue detail

The WordPress REST API provides powerful functionality for interacting with your website's data, allowing developers to create interactive and dynamic web applications. However, when the REST API endpoint is publicly available, it can pose significant security risks if not properly secured.

## Issue background

The WordPress REST API being accessible to the public raises significant concerns due to the potential risks involved. This includes the ability for unauthorized parties to gather information about the themes and plugins being used. Moreover, if the API is not properly configured, it could lead to user enumeration, leakage of sensitive data, and unauthorized individuals gaining the capability to execute malicious actions, thus compromising the security and functionality of the website.

## Issue remediation

Limit access to the WordPress REST API endpoints to authorized users only. Implement authentication mechanisms such as OAuth 2.0 or API keys to control access. This ensures that only authenticated users or applications can interact with the API.


## Like what you see?

<p align="center">
<a href="http://10up.com/contact/"><img src="https://10up.com/uploads/2016/10/10up-Github-Banner.png" width="850"></a>
</p>
