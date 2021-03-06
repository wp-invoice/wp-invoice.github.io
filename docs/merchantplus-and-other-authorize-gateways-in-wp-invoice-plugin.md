---
title: MerchantPlus and Other Authorize Gateways in WP Invoice plugin
sidebar_title: MerchantPlus and Other Authorize Gateways
permalink: /docs/merchantplus-and-other-authorize-gateways-in-wp-invoice-plugin/
---

![Authorize.Net and merchantplus gateways](https://storage.googleapis.com/media.usabilitydynamics.com/authplus.jpg)
***
To enable payments with credit cards and be able to view this area, the **MerchantPlus.com and other Authorize.net Gateways** checkbox under **Payment Gateways** must be checked. WP-Invoice works with any payment processor that has a redirect gateway similar to MerchantPlus or Authorize.Net.

* * *

*   **Gateway Username:** Enter the username your credit card processor has given you.
*   **Gateway Transaction Key:** Enter the secure key generated by your credit card processor, for accessing your gateway. You should be able to find / generate this on your gateway’s control panel.
*   **Gateway URL:** Enter the redirect URL for your gateway. You should be able to find this on your gateway’s control panel. We have included the URLs for MerchantPlus, Authorize.Net and Authorize.Net Developer (for testing purposes). If you are using one of these gateways, click on the name of the gateway underneath the field and the URL will automatically appear in the field.
*   **Recurring Billing Gateway URL:** If you want to accept recurring payments with your gateway, enter the Recurring Billing Gateway URL here. You should be able to find this on your gateway’s control panel. Note that usually it is different than the normal Gateway URL (almost always with Authorize.Net), unless specified by the processor. We have included the URLs for Authorize.Net ARB and Authorize.Net ARB Testing (for testing purposes). If you are using one of these gateways, click on the name of the gateway underneath the field and the URL will automatically appear in the field. Be advised, test credit card numbers will be declined even in test mode.
*   **Test / Live Mode:** Select “**Test - Do Not Process Transactions**” if you want to do some test payments before you enable live payments. Select “**Live - Process Transactions**” if you want to enable real payments or when you are done testing. **ATTENTION:** Do not forget to change this setting after you are done testing or you will not be credited any money for invoice payments!
*   **Delimiter Character:** Enter the delimiter character for your gateway. Consult your gateway documentation to find out if you should enter something here. If the transactions are not going through, and all other settings are correct, the character you have entered here will most probably be wrong.

*   **Encapsulation Character (Optional):** (For some processors like Authorize.Net you should leave this blank) Some processors will need you to enter a special character here. Consult your gateway documentation to find out if you should enter something here. If the transactions are going through but there are strange responses, the character you have entered here will most probably be wrong.
*   **Email Customer (on success):** Select “Yes” to automatically send an email to customers after a successful transaction.
*   **Merchant Email (Optional):** Enter an email address that will receive a copy of the client confirmation email sent on success. If a value is set, an email will be sent to that address as well as the address(es) configured in the Merchant interface.
*   **Customer Receipt Email Header:** Consult your gateway documentation to find out if you should enter something here.
*   **Security MD5 Hash:** An MD5 hash that may be required by your processor’s gateway. Consult your gateway documentation to find out if you should enter something here.
*   **Delim Data:** Specifies if the response data will be separated with the delimeter set on Delimiter Character (#6) or not. You should be able to find if you should enable this, on your gateway’s control panel.
*   **Silent Post URL:** This URL is created automatically by WP-Invoice. As soon as a transaction is completed, your gateway sends a POST request to your WordPress installation (this URL). You should update your gateway settings so that it sends Silent POST requests to this URL.

![](//storage.googleapis.com/media.usabilitydynamics.com/Screen-Shot-2011-12-12-at-10.55.52-AM.png)