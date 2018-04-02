---
title: "WP-Invoice: PDF"
sidebar_title: "Home"
slug: pdf/index
description: Creates PDF versions of your invoices, receipts and that you can easily email and print.
image: //storage.googleapis.com/media.usabilitydynamics.com/2014/10/23c427c6-wpinvoice-extension-pdf-icon-300x300.png
repo_url: https://github.com/wp-invoice/wp-invoice-pdf
module: "WP-Invoice: PDF"
module_slug: pdf
---

###Welcome to the WP-Invoice: PDF wiki!

PDF Add-on allows you to easily generate PDF versions of your invoices, receipts and quotes. The generated files can be used as e-mail attachments, or displayed as links on the secure invoice pages. The Add-on is shipped with four unique PDF layouts.

![PDF Settings](https://storage.googleapis.com/media.usabilitydynamics.com/Screen-Shot-2011-12-19-at-3.30.01-PM.png "PDF Settings")

### Setting up the PDF functionalities

Here is a description of the various options you will need to set up to have the PDF Invoices and Receipts feature work.

**Do not automatically insert PDF link on bottom of invoices**: the PDF Invoices and Receipts feature will automatically add a link to the PDF version of each invoice or receipt, on the bottom of the invoice display page, in the front-end of your installation. By checking this, the link will not appear on the page.

**Display logo in the PDF**: If checked, a field will appear, where you should enter the URL of your logo. It will appear on your PDF invoices, quotes and receipts.

**Display business name and address**: If checked, the business name and address you have set on the Main invoice settings tab, will appear on the header of your PDF file (invoice, quote or receipt).

**Display invoice description**: If checked, the invoice’s description text (the free text on the invoice edit page) will appear under the header.

**Select template**: When developing the PDF Invoices and Receipts Feature, we thought that you probably wouldn’t like an ugly, simple layout for your invoices, so we took the liberty to design and implement three different invoice designs for you to choose from. So your options on the drop-down field here are three: Traditional, Modern and Bold (extra modern).

**Tip**: Create a dummy invoice with item descriptions and everything and try out the invoice templates, before you choose.

**Display Terms and Conditions**: If checked, a text filed will appear under the checkbox, where you will be able to insert your Terms and Conditions, that will appear on all invoices.

**Display Notes**: If checked, a text filed will appear under the checkbox, where you will be able to insert your Notes. They will appear on all invoices.

### Adding the PDF link to messages

To add a link to the PDF invoice / receipt to your message templates, just use the **%pdf%** code in a message template. It will be replaced with a link to the PDF itself, in the message's body. Note that this will not add the PDF file as an attachment to the message, but a hyperlink that leads to the PDF on your website. Attaching the PDF is **not available** right now.

### PDF templates customization

Please, note, that any code customizations you make on your own risk. We won’t debug your templates if they look bad or cause issues.

*   To add new template just copy existing in /core/template/pdf_quote*.php and place it near. Rename file to something like pdf_quote_new.php and change “Template Name” inside to something like “Template Name: New One”. That’s it.
*   For customizing existing one – copy template you need to the “wpi” folder the root of your theme (Create it if it doesn’t exist) and change there whatever you need.

### Example of Invoice PDF

![PDF Example](https://storage.googleapis.com/media.usabilitydynamics.com/2014/10/f6a29c31-invoice-pdf.png "PDF Example")
