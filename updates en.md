# Updates

## 5.2.1 Jan 24, 2023

### Maintenance release

### Corrected bugs:

- Argument 1 passed to XF\Mvc\Entity\Entity::addCascadedSave() must be an instance of XF\Mvc\Entity\Entity, null given, called in src/addons/XFA/RMMarketplace/Pub/controller/Dashboard.php on line 86

## 5.2.0 Jan 11, 2023

### Bug fix and new feature

### Corrected bugs:

- Call to a member function getCommunicationDataFromType() on null - src/addons/XFA/RMMarketplace/Service/Purchase/Notify.php:79

### New features:

- Automatic license key generation capability, activated through an option and configurable per resource

## 5.1.1 Jan 2, 2023

### Maintenance release

### Corrected bugs:

- ErrorException: Job XFA\RMMarketplaceDiscountsApplier: [E_WARNING] Attempt to read property "type" on null src/addons/XFA/RMMarketplace/Job/DiscountsApplier.php:36
- Error: Call to a member function fastUpdate() on null src/addons/XFA/RMMarketplace/Job/DiscountsApplier.php:100
- ErrorException: [E_NOTICE] Undefined variable: resourceIds src/addons/XFA/RMMarketplace/Job/DiscountsApplier.php:79
- Error: Call to a member function getCommunicationDataFromType() on null - src/addons/XFA/RMMarketplace/Service/Purchase/Notify.php:72
- Resources prices reset after upgrade

> For those who upgraded to the latest version and experienced the last bug, I am very sorry for that.
> You need to revert back the prices from before the upgrade manually (if you didn't see it and already reset back to your pre-install database backup).
> I sincerely apologize for that.

## 5.1.0 Dec 31, 2022

### Bug fixes and new features, including long awaited Discounts capability

I said I would release this before the year end, and here it it is, the long awaited 5.1.0 version, introducing some new features and in particular the Discount creation capability. I hope you will enjoy this new version and I wish all of you an happy new year 2023 !

### Corrected bugs:

- ErrorException: [E_WARNING] Attempt to read property "shipping" on null src/addons/XFA/RMMarketplace/Pub/View/Invoice.php:129
- Free not displayed in grid view when resource price is 0.00
- Filter on user's license page redirects to forum index
- Free resources filter not working properly
- Error initialising PayPal communication error when seller has bypass percentage on sale permission
- ErrorException: [E_WARNING] Undefined variable $providers in src/addons/XFA/RMMarketplace/Pub/Controller/Dashboard.php at line 392
- Can’t add free shipping row in physical resources
- Fixed incorrect your purchases link in resources subnavigation

### Modifications:

- Add license button moved below dashboard tabs
- Changed grid item display layout to accommodate with discount display
- Added invoices date in invoices list
- Some dashboard tabs renamed
- Dashboard home tab removed - Index default to Stats or Sales or Licenses depending on permissions
- Terms and conditions/Invoicing dashboard tabs merged into a Configuration tab
- Option to configure the number of days after which unpaid purchases are automatically pruned (instead of 1 day fixed)
- Modified permissions interface groups

### New features:

- Discount creation capability
- Capability to manually validate an unpaid purchase
- Capability to add license from resource page through resource menu
- Warning message in purchase form when user owns an expired license asking if he would like to renew instead
- Option in digital products to disallow renewal of license after expiration
- Time period filter added in purchases list
- Sales log export to .xlsx or .csv from dashboard sales page
- Optional automatic blocking of user sales X days after monthly percentage on sale invoice generation if unpaid (xF payment profile solution)
- Capability to disable/enable sale of a resource
- Added new supported xF payment profiles: Mollie, BTCPay
- Permission based capability for the seller to select which communication means to use (email/conversation) upon purchase/refund
- Permission based capability for the seller to customise the title/message sent upon purchase/refund from dashboard configuration tab
- New status filter (unpaid, validated, refunded) in dashboard view sales page

## 5.0.4 Jan 15, 2022

### Maintenance release

### Corrected bugs:

- ErrorException: Template error: [E_WARNING] Attempt to read property "group_id" on null src/addons/XFA/RMMarketplace/Listener.php:175

## 5.0.3 Jan 5, 2022

### Maintenance release

### Corrected bugs

- ErrorException: Template error: [E_WARNING] Attempt to read property "xfa_rmmp_type" on null src/addons/XFA/RMMarketplace/XF/Entity/Thread.php:79
- ErrorException: Template error: [E_WARNING] Undefined variable $resource src/addons/XFA/RMMarketplace/XF/Entity/Thread.php:79
- Shipping amount displayed in sales list even when null
- User address required in PayPal payment profile for Digital products

## 5.0.2 Dec 30, 2021

### Maintenance release

### Corrected bugs

- Payment providers option description incorrect in admincp (data is encrypted)
- XF\Db\Exception: MySQL statement prepare error [1054]: Unknown column 'shipping' in 'field list' in src/XF/Db/AbstractStatement.php at line 228
- For Paypal XF payment profiles only require address if product is of physical type

Coinbase Commerce Integration payment profile is now supported following our Core add-on 1.11.1 release.

## 5.0.1 Dec 1, 2021

### Maintenance release

### Corrected bugs:

- ErrorException: Template error: [E_USER_WARNING] Cannot call method isForSaleInMarketplace on a non-object (NULL) src/XF/Template/Templater.php:1176
- Additional info data input displayed for other product types than physical

## 5.0.0 Nov 24, 2021

### Major feature changes - xF payment profiles support

This new version is a major feature changes release which contains an extensive set of improvements and in particular the implementation of a new payment mode based on xF payment profiles (either admin/user configured).

We would like to thank @frybread for funding the development of this new feature.

It was extensively tested but we recommend you to first test this new version on a development environment before going live. And don't forget to backup your files and database prior to performing the upgrade.

Detailed changelog is provided here below.

### Corrected bugs

- Default image incorrectly displayed when in grid layout mode when friendly urls option is activated
- Incorrect grid view box layout with stars not fitting on a single line

### Modifications

- Put buy and download buttons in a group when both are displayed
- Permissions split into two categories: standard permissions/moderator permissions
- Rewording of some permissions text

### New features

- Revamped options page with tabs sorting
- Revamped purchase confirm form
- Featuring durations/featuring purchases links changed in admincp
- Price added next to duration on admincp featuring purchases page
- Capability to purchase a digital product for a friend (permission based)
- Seller/Buyer/Valid licenses postbit indicators in resources discussion threads (style properties based)
- New permissions
  - Bypass percentage on sale permission
  - Maximum number of items on sale
- Configurable automatically displayed prefixes in resources list to identify digital products/services/physical products/Out of stock physical products
- Invoice preview button in Invoicing Dashboard page
- New payment handling mode based on xF payment profiles
  - Payment profiles either based on admin ones or user front-end side configurable ones
  - Supported methods:
    - Back-end configured methods: Any
    - Front-end configured methods: Paypal, Braintree, Stripe, 2checkout (Get in contact with us for more payment methods addition)
  - Monthly invoices generation for percentage on sales payment by users based on effective sales
  - Email/alerts sent on invoice generation/payment/refund
  - User front-end side payment profiles configuration from dashboard
  - User front-end side payment profiles configuration encrypted into database
  - Your invoices page on front-end side
  - Invoices list page on back-end
  - Send reminder from invoices list for unpaid invoice
- Simple shipping costs handling
  - Input location/cost when editing resource
  - Shipping cost automatically added to item price upon purchase
