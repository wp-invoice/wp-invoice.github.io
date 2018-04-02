---
title: Setting up Recurring billing in WP Invoice plugin
sidebar_title: Setting up Recurring billing
permalink: /docs/setting-up-recurring-billing-in-wp-invoice-plugin/
---

This guide will help you to understand **WP-Invoice Recurring Billing** options and general work flow. **WP-Invoice Recurring Billing** User Interface has been changed in _version 3.08.9_ of **WP-Invoice plugin**. It became more user friendly and logical.

### How does it work

Basically, WP-Invoice doesn't handle the whole process of recurring payments or subscriptions. It just initiates them and then listens for payment notifications from payment services (in case if webhooks set up properly). Subscription initiation happens when users pay recurring invoice first time (actually, they do not need to pay that invoice again).

### Setting up

First you have to enable recurring billing options for the plugin globally. Go to **Invoice -> Settings -> Main** and find there a section **Advanced Settings**. In this section find a checkbox labeled as **Show recurring billing options.** Check it and click _Save All Settings_ button below.

The next step is creating the recurring invoice. Create new invoice by clicking **Invoice** -> **Add New**. You'll see **E-mail Address** ﻿field. Start **typing** some user's name or email and then select an item you need from populated dropdown. Click **Create New.

**﻿﻿Now we have newly created invoice with default options set.﻿﻿Set﻿some title since it is required.﻿ Then find **Publish** metabox﻿(top right corner) and check there a checkbox labeled as **Recurring Bill.** ﻿New settings will appearbelow﻿:

![](https://storage.googleapis.com/media.usabilitydynamics.com/2016/09/invoice-recurring.png)

As you can see each payment service has it's own Recurring/Subscription settings. This is because each service provides different options. Configure one/all recurring options and select which one you want to use for current invoice below in **Payment Settings** metabox (Default Payment Option).

### Reflecting payments on the site

As was mentioned **WP-Invoice** plugin listens to payment services for payment notifications. This is actually how plugin knows about subscription payments made. To be sure payments will be reflected in invoice lo just set up 'webhooks' in you merchant accounts. Webhook URL you can find in **Settings** -> **Payment** under each of payment gateways.

*   Authorize.net - Silent Post
*   PayPal - Instant Payment Notifications
*   2Checkout  - URL/INS URL
*   Stripe - Webhook URL

###These payment gateways do not support Recurring Billing
*   InterKassa
*   Mijireh Checkout
*   PayPal Pro
*   USA ePay

### Why it is impossible to use multiple Payment Methods for Recurring Billing

As was said above, each payment service provides different Subscription options like Intervals, Cycles or Counts etc. They are not the same for all Payment Methods.

So, let's imagine that it is possible and you have configured recurring options for all gateways. For instance: you need to charge user every week 5 time and you have allowed people to select between _Authorize.net (Credit Card)_ and PayPal and configured **Authorize.net ARB** and **PayPal Subscriptions** the following way:

*   Authorize.net ARB - **Bill every - 1 Day(s)** (since there is no ability to set Week(s)) **Billing Cycles - 5**

*   PayPal Subscriptions - **Bill every - 1 Week(s)** **Billing Cycles - 5**

Now users can pay recurring invoice by Authorize.net or PayPal but with the difference in billing interval (1 day and 1 week). ...Confusing, huh? Event more, results of subscription initiation will be unexpectable for users.

So, this is the cause of that there is no ability to set multiple payment methods for recurring invoices. You can set only one payment method for recurring invoice to avoid misunderstanding.