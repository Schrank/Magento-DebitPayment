DebitPayment
=====================
This extension allows shop owners to provide the payment method "DebitPayment" to their customers.

Facts
-----
- version: 0.5.4
- extension key: DebitPayment
- [extension on Magento Connect](http://www.magentocommerce.com/magento-connect/debitpayment.html)
- Magento Connect 1.0 extension key: magento-community/DebitPayment
- Magento Connect 2.0 extension key: http://connect20.magentocommerce.com/community/DebitPayment
- [extension on GitHub](https://github.com/therouv/Magento-DebitPayment)

Description
-----------
This extension allows shop owners to provide the payment method "DebitPayment" to their customers.
This includes:
- Complete order via DebitPayment
- Find the correct German bank name given by the entered routing number
- Save account data encrypted in database to pre-fill checkout fields on further checkouts
- Export all DebitPayment orders as CSV file or DTAUS file

Requirements
------------
- PHP >= 5.2.0

Compatibility
-------------
- Magento >= 1.6
- Versions below should work to version 1.4 without any problems but it is not actively tested.

Installation Instructions
-------------------------
1. Install the extension via Magento Connect with the key shown above or copy all the files into your document root.
2. Clear the cache, logout from the admin panel and then login again.
3. You can now enable the payment method via *System -> Configuration -> Sales -> Payment -> DebitPayment*

Uninstallation
--------------
To uninstall this extension you need to run the following SQL after removing the extension files:
```sql
  DELETE FROM `core_resource` WHERE code = 'debit_setup';
  DELETE FROM `eav_attribute` WHERE attribute_code = 'debit_payment_acount_update';
  DELETE FROM `eav_attribute` WHERE attribute_code = 'debit_payment_acount_name';
  DELETE FROM `eav_attribute` WHERE attribute_code = 'debit_payment_acount_number';
  DELETE FROM `eav_attribute` WHERE attribute_code = 'debit_payment_acount_blz';
  DROP TABLE `debit_order_grid`;
```

Support & Feature-Wishes
------------------------
If you have any issues or you are missing an feature with this extension, please open an issue on [GitHub](https://github.com/therouv/Magento-DebitPayment/issues). Thank you.

Contribution
------------
Any contribution is highly appreciated. The best way to contribute code is to open a [pull request on GitHub](https://help.github.com/articles/using-pull-requests).

Developer
---------
Rouven Alexander Rieker
- Website: [http://rouven-rieker.com](http://rouven-rieker.com)
- Twitter: [@therouv](https://twitter.com/therouv)

Licence
-------
[Open Software License (OSL 3.0)](http://opensource.org/licenses/osl-3.0.php)

Copyright
---------
(c) 2012 Rouven Alexander Rieker