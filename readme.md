# Basic Excel Import For OpenCart v3.0


## CHANGES

* Added Database External Column Support
* Added Seo Metod Support
* Changed Image lookup metod
* Fixed some bugs

## INSTALLING

**OC MOD INSTALLING**

When you download files, you will find "excel_import.ocmod.zip" file.

* Login you administration panel,
* Go to **Extensions -> Installer**
* Select "excel_import.ocmod.zip" file and upload.
* Go to **Extensions -> Modifications** click refresh button on top right
* After installing module go to **System -> Users -> User Groups -> Edit User Group**
* Find "extension/import/excel" both Access Permisison and Modify Permisison lists and check it.
* It's Done !

**Standart Ftp Uploading**

**NOTE :** If you don't use oc_mod install method, you should add a link manually to navigation for access to module. Because there is no modification for edit menu items.

**Link :** index.php?route=extension/import/excel&user_token=*******

* Download file from repository
* Find "upload" folder and upload inside files to your opencart root dir.
* After upload files, go to **System -> Users -> User Groups -> Edit User Group**
* Find "extension/import/excel" both Access Permisison and Modify Permisison lists and check it.
* It's Done !

## Some Tricks

* If used category names not saved before to opencart, excel importer will add categories automatically,
* If product option's and option values not saved before to opencart, excel importer will create options and values automatically,
* System set seo url automatically based on product name
* you can manage all settings from settings panel, take a look screenshots.

![SCREENSHOTS](https://emreacar.com.tr/sources/2.png)

![SCREENSHOTS](https://emreacar.com.tr/sources/5.png)

![SCREENSHOTS](https://emreacar.com.tr/sources/1.png)

![SCREENSHOTS](https://emreacar.com.tr/sources/4.png)




## USAGE

* First we must set some settings before upload an excel file,
* Choose which product form data assign to in your excel,
* After edit all rows or just using in excel, save settings,
* Select your upload file and submit form.

## USAGE NOTES

**CATEGORIES**

You can use only one row for a product, so if you want to set product's category information from excel read above.

**EX. product info with product categories**


| COLUMB A | COLUMB B | COLUMB C | COLUMB D |
|----------|----------|----------|----------|
|Product Model | Product Name | Main Category Name | Sub Cat. Name | Sub Cat. 2 Name |


In this example our products goes to; **Main Category -> Sub Category -> Sub Category**, but if you whant to **set multiple main category** take a look example above.



| COLUMB A | COLUMB B | COLUMB C | COLUMB D |
|----------|----------|----------|----------|
|Product Name | Main Cat\|Main Cat 2 | Sub Cat 1\|Sub Cat 2 | Sub Cat 1,2\|Sub Cat 2,2|


In this example our product goes to; **Main Cat -> Sub Cat 1 -> Sub Cat 1,2** and **Main Cat 2 -> Sub Cat 2 -> Sub Cat 2,2** categories.

Sortly for multiple category you can **use sperator** " | " between category names.


**Product Options**

For add an option to product, you should add new row for product option. If another row has same product model, system get this row as product option.

**Example for product option**

| COLUMB A | COLUMB B | COLUMB C | COLUMB D |
|----------|----------|----------|----------|
| Model001 | Prod. Name | 127.00 | 10       |
|----------|----------|----------|----------|
| Model001 |  OPTION NAME\|OPTION VALUE NAME | +50.00   | 5 |
|----------|----------|----------|----------|
| Model001 | OPTION NAME\|OPTION VALUE 2 NAME  | +50.00   | 5 |


If you want to add more options you can add more row What has to same model number.

* You should use same quantitiy columb for options quantitiy info.
* You should use same price columb for options price info.
* If you want to " - " prefix for price, you can set price columb "-50.00"
* Dont use curreny sym in price columbs.