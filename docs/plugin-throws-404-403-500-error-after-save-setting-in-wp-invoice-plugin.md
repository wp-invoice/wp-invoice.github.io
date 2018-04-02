---
title: Plugin throws 404 403 500 error after Save Setting in WP Invoice plugin
sidebar_title: Plugin throws 404 403 500 error after Save Setting
permalink: /docs/plugin-throws-404-403-500-error-after-save-setting-in-wp-invoice-plugin/
---

It is the one of the most frequently asked question. When you try to save settings or first time setup page you got 404 or some another error.

We did some investigation and found that the cause is mostly connected to Apache mod_security module which goes with some hosting/server plans by the default. http://www.modsecurity.org/

The module has settings called Rules that are monitoring the access requests to your site. If mod_security rule decides that request data or URL or something else is dangerous on their opinion then it throws error preventing further access to the site.

The problem is that rules can be customized the way nobody expects. We cannot change the way setting are saving to satisfy any mod_security rule.

That is happening with invoice save settings action for some hosting/server plans. e.g. DreamHost, GoDaddy.

The only way to fix that is to contact hosting provider to see mod_security logs for details that will help to determine which rule is fired for your case and try to fix it or turn off.

Also to get around this, you can temporarily disable mod_security, configure your WP-Invoice setup, and then re-enable mod_security. The easiest way to temporarily disable mod_security is to create an .htaccess file in the document root of the web server with the following contents:

```
SecFilterEngine Off
SecFilterScanPOST Off
```
Save that file and restart Apache. After you take care of the final setup of WP-Invoice, make sure to delete or rename that .htaccess file and restart Apache. If you don't remove that file and restart the server, Apache will be wide open and insecure.  Remember: don't forget to turn mod_security back on.

We guarantee that our code doesn't do any dangerous actions. It just posts the data to be saved.