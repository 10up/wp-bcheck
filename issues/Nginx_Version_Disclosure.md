# Nginx version exposure in upload folder

## Issue detail

The exposure of the upload folder allows unauthorized users to view and potentially manipulate sensitive files uploaded to the site, posing risks such as data breaches, unauthorized access, and malware injection.

## Issue background

WordPress sites typically utilize an "upload" directory to store media files such as images, videos, and documents. However, if this upload directory is publicly accessible, it means that anyone can view and potentially interact with the files stored within it. This can occur due to misconfigurations, improper permissions, or vulnerabilities in themes or plugins. Attackers can exploit this exposure to gather sensitive information, upload malicious files, or execute attacks such as directory traversal or file inclusion.

## Issue remediation

Adjust server configurations or employ WordPress plugins to limit public access to the upload folder. Make sure to disable directory listings and grant access only to authorized users who need to interact with files in the upload directory.

## Like what you see?

<p align="center">
<a href="http://10up.com/contact/"><img src="https://10up.com/uploads/2016/10/10up-Github-Banner.png" width="850"></a>
</p>
