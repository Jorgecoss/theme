Version 1.0.4

- Add the logo to checkout page
- Add Amp feature

You can ignore this path if you are new, if you have been using the theme and want to update to this version, do the following steps:

- Upload app/ folder in patch_theme_version_1.0.4/ folder to magento root, override old files
- Connect to SSH, navigate to magento root then run:
    + php bin/magento module:enable MGS_Amp
    + php bin/magento setup:upgrade
    + rm -rf var/* ( delete the content of var folder )
    + rm -rf generated/* ( delete the content of generated folder )
    + rm -rf pub/static/frontend/Mgs/* (delete the content of pub/static/frontend/Mgs/ folder)
    + php bin/magento setup:static-content:deploy -f
    + php bin/magento cache:clean