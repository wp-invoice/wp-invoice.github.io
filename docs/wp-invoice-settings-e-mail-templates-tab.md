---
title: WP Invoice Settings E-Mail Templates Tab
sidebar_title: E-Mail Templates Tab
permalink: /docs/wp-invoice-settings-e-mail-templates-tab/
---

Here you can create, edit and delete email templates that will be used for various manual notifications. WP-Invoice automatically creates the most common templates for you, you only need to edit them so they suit your needs better.

* * *

[![the email notification settings tab](https://storage.googleapis.com/media.usabilitydynamics.com/Screen-Shot-2011-12-12-at-1.57.42-PM.png)](https://storage.googleapis.com/media.usabilitydynamics.com/Screen-Shot-2011-12-12-at-1.57.42-PM.png)

* * *

## Dynamic Parameters

The email template system of WP-Invoice accepts some dynamic parameters that you can place in the subject or the content field and they will be replaced with text or hypertext on the actual email the recipient gets. You have to use the parameters as they appear on the list, with the % symbol on the left and right of the words. Here is a list of these dynamic parameters and what they are replaced with:

*   **%subject%** is replaced with the invoice title (subject) of the related invoice (the one the email notification is about).
*   **%recipient%** is replaced by the name of the email’s recipient for the related invoice.
*   **%type%** is replaced by the word of current object type (invoice, recurring, quote).
*   **%amount%** is replaced by the total amount of the related invoice.
*   **%description%** is replaced by the invoice description / content (if set). Note that this is the free text that you create while adding an invoice, not the actual invoice.
*   **%link%** is replaced by a link to the online page of the related invoice. 
*   **%link%&format=pdf**  Download a PDF invoice
*   **%business_name%** is replaced by the business name you have set on WP-Invoice’s settings.
*   **%business_email%** is replaced by the business email you have set on WP-Invoice’s settings.
*   **%creator_name%** is replaced by the full name of the related invoice’s creator.
*   **%creator_email%** is replaced by the email account of the related invoice’s creator.
*   **%due_date%** is replaced by the related invoice’s due date (if set).
*   **%type%**  Replaced by Invoice Type. (invoice, recurring invoice, quote)
*   **%pdf%**  URL to PDF version of invoice.

## Email Template Entries

There are three fields in each template entry: 

*   **Name:** This is the name that is used to distinguish the email template in the system. It cannot take any dynamic parameters.
*   **Subject:** This is the subject of the notification email that the recipient will get. You can use dynamic parameters here.
*   **Content:** This is the actual email that the recipient will get. You can (and really should) use dynamic parameters here.

####Here is some example of default template:

[![The email content field](https://storage.googleapis.com/media.usabilitydynamics.com/Screen-Shot-2011-12-12-at-1.58.02-PM.png)](https://storage.googleapis.com/media.usabilitydynamics.com/Screen-Shot-2011-12-12-at-1.58.02-PM.png)