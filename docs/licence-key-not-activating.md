---
title: Licence Key not activating
sidebar_title: Licence Key not activating
permalink: /docs/licence-key-not-activating/
---

By default you can use 2 domains for each license. But if you copied your database to another domain you will have an issue with our products activating.  Reason being, an instance hash is stored in the options table that is related to the URL of the site on which the product was initially activated.

You will need to delete these options keys form the database `(wp_options)` and reactivate the license(s) again.

---

You can delete them at this url -  `yoursite/wp-admin/options.php`.

![](https://storage.googleapis.com/media.usabilitydynamics.com/2016/10/instance-license.jpg)

---

If you use `wp-cli` you should be able to remove the extra options like so:

```
wp option delete wp-propertyslideshow:instance
wp option delete wp-propertywalkscore:instance
wp option delete wp-propertyagents:instance
```

If you do not have `wp-cli` available, make changes directly to the database. As usual, be sure to make a backup first.
