---
title: "WP-Invoice: Power Tools"
sidebar_title: "Home"
slug: power-tools/index
description: Make you invoicing solutions more powerful with WP-Invoice and Power Tools. Sales charts, import and export ability!
image: //storage.googleapis.com/media.usabilitydynamics.com/2014/10/4414bbd6-power-tools2-300x300.jpg
repo_url: https://github.com/wp-invoice/wp-invoice-power-tools
module: "WP-Invoice: Power Tools"
module_slug: power-tools
---

### Welcome to the WP-Invoice: Power Tools wiki!

This Add-on allows you to export your invoices in the XML and JSON formats and import data from other WP-Invoice installations. Furthermore, it provides a graphic visualization of your sales, filtered by day, week or month.

###  Export Options

**Default Format**: Here you can choose the data format you wish to export your invoices to, between XML and JSON. Different systems accept different formats, so make sure that you know what format is accepted from the system you will import to and set it here.

**XML Charset**: With the checkbox checked, the resulting XML file will use the charset of your WordPress installation. If you uncheck the box, you will be able to enter the charset of your choice in an input field to be used instead. UTF-8 should be recognized by most systems but in case yours requires something different, you can set it here (XML format only).

![](https://storage.googleapis.com/media.usabilitydynamics.com/2013/02/tools_menu.jpg)

_You can find Import/Export functionality in Tools menu of WordPress._

**XML Version**: Here you can set the XML version you want your resulting XML file to have set. Once more, this depends on your system, but the default value should work for 9/10 systems (XML format only).

**Log History**: If you check the checkbox labeled "Export Invoice log history", any invoice history logged on your invoices will be exported as well. If your system does not have use for the history, uncheck this, as it will reduce your export's file size.

**Filename Format**: Here you can set the way you want your export's file to be named, by using any of the allowed tags: [blog_name], [month], [day], [year], [hour], [minute], [second] and [timestamp]. This is for your organization mostly, if you keep all exports somewhere.

### Import Options

**Log History**: If you check the box labeled "Add import log item", imported invoices will include a new line in their history log with the name of the user who imported them and the time. Great for distinguishing which invoices were imported and which not.

**Recipients**: Here you can set whether to use the recepient info (name, etc) set on your system on import, or change it to the info from the import file.

![Import and Export Settings](https://storage.googleapis.com/media.usabilitydynamics.com/2013/02/wpi_import_settings.png "Import and Export Settings")

First you need to set if you want to override the recipient information if it already exists in your installation. If the box stays unckecked, the imported recipient's info will remain as-is in your installation. If you check it, the info will be replaced by the one on the invoice. After this, you need to set how to handle recipients who do not exist in your installation. By setting the "If Recipient does not exist" dropdown, you can chose between creating a new recipient (with the info from the imported invoice) or use an existing recipient (from your system) for all imported invoices where the recipient is unknown to your installation, by setting the email of the user you want to assign the invoices to.

Finally, you can set the user role that will be assigned to newly created recipients, in the last dropdown.

### Sales Visualization

![Sales Visualization](https://storage.googleapis.com/media.usabilitydynamics.com/2013/02/visualize.png "Sales Visualization")

Another functionality that the Power Tools for WP-Invoice provides, is the ability to visualize your sales, filtering sales by day, week or month and view your sales chart in different zoom from 1 day to all time your existence.

You can find this button on filter box of your invoices. You also will have ability to visualize your sales, filtered by type, status, recipient and date of payments.

![](https://storage.googleapis.com/media.usabilitydynamics.com/2013/02/visualize-sales-button.png)
