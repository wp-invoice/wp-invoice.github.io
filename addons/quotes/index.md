---
title: "WP-Invoice: Quotes"
sidebar_title: "Home"
slug: quotes/index
description: The Quotes Add-on let’s you automate your workflow by creating quotes and letting your clients ask questions regarding quotes directly on your website. Once a quote is approved, it is converted to an invoice with a single click.  
image: //storage.googleapis.com/media.usabilitydynamics.com/2014/10/6ce103ff-wpinvoice-extension-quotes-icon-300x300.png
repo_url: https://github.com/wp-invoice/wp-invoice-quotes
module: "WP-Invoice: Quotes"
module_slug: quotes
---

Until the release of this feature, we used two terms to describe invoices, depending on if they are paid or not: Invoices and receipts. One of the main problems of the users though, was the creation of quotes. It’s an organizational matter mostly. Until now, the professional (you) had to create an invoice, then the client would have to take a look, accept it and pay. What if the client had an objection though? They would have to send an email, then you would have to change the invoice and this process would be repeated again and again until the client was ready to pay. Now, you can mark invoices as quotes (that cannot be paid until they are accepted by the client).

### Why?

With the way modern online businesses evolve, especially with the help of the Internet, contact with the client is gradually becoming less, more digital and ideally, the system you use should make all communications easy to find and manage. That’s why with the Quotes invoice, we have implemented a comment system with which, your client can leave questions / comments to you and you can reply to them until everyone is happy. Then you change the quote to an invoice, and the client can pay it. And of course, you get email notifications for new questions. This way the whole process is more simplified, the client does not have to send emails, just to view the invoice and add a comment. And you get to keep the conversation archived for future reference. Win-win.

### How it Works?

**1.** The Quotes Premium Feature for WP-Invoice uses the invoice editing layout to manage quotes and discussions so you won’t see a separate page. Once installed, you can create a quote exactly the way you create a normal invoice with the difference that you have to click the “Quote” checkbox on the “Publish” metabox of the invoice edit page.

![](https://storage.googleapis.com/media.usabilitydynamics.com/publish.png)

**2.** Once you save the entry as a quote, the client will be able to post comments in the front-end like so:

![](https://storage.googleapis.com/media.usabilitydynamics.com/frontend-question1.png)

**3.** You instantly get an email notification for that. Then you can reply to the question and you can see the whole conversation on the invoice edit page in the comments section ( see image ).

![](https://storage.googleapis.com/media.usabilitydynamics.com/comments1.png)

**4.** After you are done with the conversation and the client is happy with the quote, you just edit it and unmark the quote field. That disables further commenting and enables payment options.

### Quotes Options

*   **Make recipients to be authorized to be able to Accept Quote.** - By default quote recipients do not have to sign in before Accepting the quote you sent to them. Tick this option if you need them to be logged in.

*   **Add "Terms & Conditions" checkbox to Quote page.**  - This option allows you to add "Terms & Conditions" checkbox to every Quote page. Be sure you have specified Terms page ID.
    **"T&C" Page ID** - Numeric value of WordPress page ID that has "Terms & Conditions".

### Customization

If you are going to use custom Page Template for displaying Quote Responses and Response box then use these WordPress functions during the development of your Theme Template:

*   **wp_list_comments** - for displaying Responses. Find out how to use it [here](http://codex.wordpress.org/Function_Reference/wp_list_comments).
*   **comment_form** - for displaying Response Box. Find out how to use it [here](http://codex.wordpress.org/Function_Reference/comment_form).
