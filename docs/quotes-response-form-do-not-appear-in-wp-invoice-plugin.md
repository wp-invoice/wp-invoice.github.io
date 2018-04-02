---
title: Quotes response form do not appear in WP Invoice plugin
sidebar_title: Quotes response form do not appear
permalink: /docs/quotes-response-form-do-not-appear-in-wp-invoice-plugin/
---

In most of cases issue is in that your Page Template that you use for Invoices/Quotes does not support comments.

Read this to understand how to add comments support for page template:[http://codex.wordpress.org/Function_Reference/comment_form](http://codex.wordpress.org/Function_Reference/comment_form)

﻿The other frequent question is ‘How to display the list of existing responses?’.

So, to get responses on quote page use this standard wordpress function:

[http://codex.wordpress.org/Function_Reference/wp_list_comments](http://codex.wordpress.org/Function_Reference/wp_list_comments)

Actually, these function usually used for regular wordpress post types. You can find code examples in default themes ‘Twenty Ten’ and ‘Twenty Eleven’.