---
title: Global or specific invoice payment settings in WP Invoice plugin
sidebar_title: Global or specific invoice payment settings
permalink: /docs/global-or-specific-invoice-payment-settings-in-wp-invoice-plugin/
---

There are two places where gateway settings are stored: global in plugins Settings -> Payment and in every specific invoice at the bottom of the edit invoice page. When you create invoices they inherit gateway settings from global settings and save them for future use.

So I assume you created invoice with incorrect or empty settings first and then updated global settings. So that way you may have incorrect gateway settings in the invoice (that was created before global payment settings updated) you are using for tests.

So just try creating new invoice or change existing invoice specific payment settings.