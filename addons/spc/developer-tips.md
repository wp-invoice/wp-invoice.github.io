---
title: "Developer Tips for SPC"
sidebar_title: "Developer Tips"
slug: spc/developer-tips
image: //storage.googleapis.com/media.usabilitydynamics.com/2014/10/21c6ccf7-wpinvoice-extension-single_page_checkout-icon-300x300.png
repo_url: https://github.com/wp-invoice/wp-invoice-spc
module: "WP-Invoice: Single Page Checkout"
module_slug: spc
---

### Actions

`wpi_spc::field_save`

Action called by invoice saving after payment process in loop through billing information. Takes one argument as Array:

*   **field** - billing item key.
*   **data** - billing item data.
*   **invoice_id** - ID of invoice generated during payment process.
*   **user_data** - array of recipient information.

### Filters

`wpi_spc::form_class`

Filters Single Page Checkout forms' class attribute. Allows to add custom class values to forms. Takes one String argument with current classes.

`wpi_spc::group_control_attrs`

Allows to add custom tag attributes for every single form input container with default class 'control-group'. Takes 3 arguments

*   **attributes** - array of default attributes.
*   **slug** - field slug.
*   **data** - array of field data.

`wpi_spc::form_input_classes`

Filters form input class attribute. Allows developers to add own custom classes. Takes 4 arguments:

*   **classes** - array of default classes.
*   **slug** - input slug.
*   **data** - array of input data.
*   **gateway** - slug of gateway.

`wpi_spc::form_actions_class`

Filters class attribute of form action sections. Allows to add custom classes for them. Takes 2 arguments:

*   **class** - default class value.
*   **gateway** - current gateway slug.

`wpi_spc::paypal_custom_amount_title`

Allows to change default label for PayPal Custom Amount field. Takes one argument with default label.

`wpi_spc_total_filter`

Filters Total value before Single Page Checkout form rendering. Takes 2 arguments:

*   **total** - current total value.
*   **settings** - Single Page Checkout settings array.

`wpi_checkout_payment_success_message`

Filters success payment message text. Takes 3 arguments:

*   **message_text** - current message text.
*   **items** - array of items which were purchased.
*   **result** - array of data of transaction response.

`spc_custom_billing_information`

Filters Billing Information. Can be used to add new fields to Billing Information section. Takes one argument of current fields array.

`wpi_spc::group_coltrol_class`

Allows you to add custom classes for form input containers with default class 'control-group'. Takes one String argument with current class.

`wpi_checkout_input_{slug}`

Multiple filter that filters input HTML before rendering according to input slug. Takes 3 arguments:

*   **input** - input HTML.
*   **slug** - input slug.
*   **data** - array of input data.

`wpi_spc::terms_label`

Allows developers to change word 'Agreement' which is label for 'agree terms' checkbox to something else. Takes one String argument with current value.

`wpi_spc::checkout_button_classes`

Filter allows developers to customize payment button classes. Takes one Array argument with default class values.

`wpi_spc::response_box_class`

Allows developers to customize classes of payment response box. Takes one String argument with default classes.