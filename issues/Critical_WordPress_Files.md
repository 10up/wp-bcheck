# Exposure of Critical WordPress Files

## Issue detail

Several critical files within the WordPress installation, including "readme.html", "wp-admin/setup-config.php", "wp-admin/install.php", "wp-admin/upgrade.php", and "wp-admin/wp-config-sample.php", are publicly accessible.

## Issue background

The "readme.html" file may contain sensitive information about the WordPress version, which can enable attackers to identify known vulnerabilities. Additionally, files such as "wp-admin/setup-config.php" and "wp-admin/install.php" can be exploited to manipulate site configurations and initiate unauthorized installations, bypassing security measures. Similarly, "wp-admin/upgrade.php" can be used to compromise the site's integrity during the upgrade process. Even the seemingly harmless "wp-admin/wp-config-sample.php" file can provide insights into site configurations, which can be utilized by attackers to tailor their attack.

## Issue remediation

If completely blocking public access to "/readme.html", "/wp-admin/setup-config.php", "/wp-admin/install.php", "/wp-admin/upgrade.php", and "/wp-admin/wp-config-sample.php" isn't possible, ensure to configure server settings or utilize access control mechanisms within WordPress. This will help restrict access to critical files. Take steps to prevent unauthorized users from accessing files like "readme.html" and "wp-admin/*.php" to mitigate the risks of information disclosure and unauthorized configuration changes.

## Like what you see?

<p align="center">
<a href="http://10up.com/contact/"><img src="https://10up.com/uploads/2016/10/10up-Github-Banner.png" width="850"></a>
</p>
