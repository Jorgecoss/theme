Version 1.0.3

- Fix not need to active the theme on localhost
- Fix missing some promo banners image
- Fix some other small issues

You can ignore this path if you are new, if you have been using the theme and want to update to this version, do the following steps:

- Upload app/ and pub/ folder in patch_theme_version_1.0.3/ folder to magento root, override old files
- Connect to SSH, navigate to magento root then run:
+ rm -rf var/* ( delete the content of var folder )
+ rm -rf generated/* ( delete the content of generated folder )
+ rm -rf pub/static/frontend/Mgs/* (delete the content of pub/static/frontend/Mgs/ folder)
+ php bin/magento setup:static-content:deploy -f
+ php bin/magento cache:clean