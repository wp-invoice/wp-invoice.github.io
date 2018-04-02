---
title: WP Invoice settings Payment tab
sidebar_title: Payment tab
permalink: /docs/wp-invoice-settings-payment-tab/
---

Here you will find the settings that will define how the various payment methods will be managed by the WP-Invoice engine.

* * *

![](//storage.googleapis.com/media.usabilitydynamics.com/2011/12/a72e0348-invoice-settings.png)

### Default Currency

Sets the default currency you will use in your invoices. Default value is U.S. Dollars.

* * *

### Default Payment Method

Here we choose the default payment method we want to use for invoice payments. 

### Client can change payment method

If set to yes, the client will be able to choose from the enabled payment methods. If set to no, the client will have the option to pay with the Default Payment Method only (described above).

* * *

### Payment Gateways

Choose which payment getaways you want to set up on your site.

*   **MerchantPlus.com and other Authorize.net Gateways:** See how to set up [here](https://github.com/wp-invoice/wp-invoice/wiki/MerchantPlus.com-and-Other-Authorize.net-Gateways).
*   **PayPal:** See how to set up [here](https://github.com/wp-invoice/wp-invoice/wiki/PayPal).
*   **Stripe**
*   **InterKassa**
*   **2Checkout**
*   **[PayPal Pro](https://www.usabilitydynamics.com/product/wp-invoice-paypal-pro)**
*   **[USA ePay](https://www.usabilitydynamics.com/product/wp-invoice-usa-epay)**
*   **[Mijireh Checkout](https://www.usabilitydynamics.com/product/wp-invoice-mijireh-checkout)** Supports for over [80 payment gateways](http://www.mijireh.com/docs/payment-gateways/).

* * *

### Manual Payment Information

If you don’t want to use payment gateways but offline payments, or if an invoice has no payment gateways enabled, the text in this field will appear as a message to the customer, offering guidance on how to pay you. Write a short text with your bank account number or any other way you want to accept the offline payment.