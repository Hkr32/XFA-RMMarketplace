# Features

## General features

- Outstanding marketplace or shop solution, either
- Source of monetization thanks to configurable percentage on sales retrieval, configured either globally or per category, as well as optional resource featuring sale.
- Fully configurable through numerous options
- Extensive rights tweaking through permissions
- Fine sale capability configuration per category:
  - Let user ask for purchases on a per resource basis (user choice)
  - Use category wide purchases (Admin choice)
  - Use forum wide purchases (Admin choice)
  - Category based allowed products configuration :
    - Select which products can be put for sale in each category. You can even select wether free products are authorized.
- Supported currencies: Based on Resources Manager currencies configuration
- New pages for buyers (with filtering): Your Purchases / Your Licences
- Seller Dashboard: a specific tabbed area for sellers to monitor and manage sales
- Users can download the resource directly after purchase
- One-click checkout form
- Various payment methods
- **[NEW 5.1.0]** Discounts feature
- Possibility to purchase more than one quantity of an item
- Capability to purchase a digital products for a friend
- Optional display of purchases number/sales number/total sales amount in membercard and profile page
- Various notifications:
  - Mails sent upon purchases or refund to the buyer, as well as in case of license status change
  - Alert sent upon purchases or refund to the seller
  - License expiration notification
- Terms and Conditions: require acceptance of the terms and conditions to buy
- New widgets: Top Purchases/Last sales
- Identification of seller and buyers in resource thread as well as capability to restrict thread access to buyers only
- Optionally activable invoicing system with PDF generation

## Resource list extension

- Price display on resources list
- New filter "Top purchased"
- Configurable prefixes
  - To identify product types (digital/physical/service)
  - To identify out-of-stock products
- Optional grid view activation to replace list view for cleaner product display
  - Based on image uploaded by the seller
  - Configurable globally or per category

## Resource view extension

- More informations on product in sidebar (Resources Manager)
- Default xF download button replaced by purchase button
- Purchase button replaced by "Register now and purchase" for non logged-in users

## Payment solutions

- Option 1 (historical): Custom Paypal solution
  - Configured from admin (global/category) or front-end side
  - Direct percentage on sales retrieval through parallel payments
- Option 2: xF Payment profiles
  - Configured from admin or front-end side
  - Safe encryption of payment configuration input by user from front-end side
  - Monthly invoiced percentage on sale retrieval
    - Automatic monthly invoice generation for percentage on sales payment with email/alerts notifications
    - Invoices page in admincp with set of tools to contact sellers
    - Invoices page on front-end side for sellers
  - Supported payment methods:
    - Admin side configured: Any
    - Front-end side configured: Paypal, Braintree, Stripe, 2Checkout, Coinbase Commerce Integration, Mollie, BTCPay. Get in touch with us to add support for more existing payment profiles if any.
- In both options: Manual payment (for cash, check...) with automatic conversation creation between buyer and seller to converge for exchanges on the payment processing details.

## Discounts [NEW 5.1.0]

- Created from seller's dashboard
- Fully configurable:
  - Title
  - Applicability: All products (if authorized to manage all sales), All seller's products, Specific products
  - Discount amount: either in percent or fixed amount
  - Time period
  - Applicability to license renewals (digital products)

## Physical Product specificities:

- Sale configuration:
  - Payment info (Paypal address)
  - Currency
  - Price
  - Quantity
  - Shipping costs
  - Terms and Conditions (with WYSIWYG editor)
- Shipment information, the status can be edited by the seller and shipment data such as a tracking url can be added.
- Stock quantity management
  - Quantity configured on add/edit
  - Option to select wether product shall continue to be sold when running out of stock
  - Alert sent to seller when product runs out of stock

## Digital Product specificities

- Sale configuration:
  - Payment info (Paypal address)
  - Licence duration (Day/month/year)
  - Currency
  - Price
  - Renewal price
  - Renewal delay
  - **[5.1.0]** Allow renewal after license has expired
  - Restriction (Yes = single copy / No = multiple copies)
  - Require url (requires the buyer to set a domain to download the product)
  - **[5.2.0]** Automatic license key generation
  - Terms and Conditions (with WYSIWYG editor)
- Capability to purchase for a friend
- Manage Licence from dashboard or user profile
  - Activate / deactivate the licence
  - Expiration date
  - Site url (enter the domain where the product will be installed)
  - Domain validity checking
- **[5.1.0]** Add license directly from resource view menu
- Alert or/and email sent upon license expiration to the holder

## Service offer specificities

- Sale configuration:
  - Payment info (Paypal address)
  - Currency
  - Price
  - Terms and Conditions (with WYSIWYG editor)

## Resource featuring features

- Available durations created through dedicated page in admincp with:
  - Duration in days, weeks, months or years
  - Amount
- Purchase of featuring by user on resource page
- Featuring purchases log on dedicated page in admincp

## Seller Dashboard features

- Direct access page for seller to manage sales, view statistics, view products, manage licenses, configure marketplace features, ...
- Statistics tab - Helps you analyse in details the sales of your products for a given period
  - Display of various statistics:
    - Number of sales
    - Gross income
    - Fees (if any)
    - Percentage on sales (if any)
  - Graphical overview of the sales evolution on the period
  - Graphical overview of the net/gross income evolution on the period
  - Highly configurable:
    - Either choose among pre-define time periods: current/previous week/month/quarter/year
    - Or select from/to through calendar popups
    - Filter by sales type (all/purchase/renewal)
    - Filter by currency
    - In case of multiple currencies selecting all will only display statistics on the number of sales.
    - Filter by resource
      When filtered on a single resource, the number of updates performed on the resource is displayed as well on the number of sales graphical overview.
- Configuration tab - Lets sellers configure various marketplace features
  - Terms and Conditions - Global Terms and Conditions for all seller products. Can be overwritten per product when creating/editing the resource.
  - Invoicing (optional) - Allows seller to configure name or company name, address, upload a logo and add any additional info to display on the invoices. Invoices generation can be activated/deactivated through this page.
  - **[NEW 5.1.0]** Communication - Allows seller to select the communication mean(s) (email, conversation or both) to be used for buyer's notification (permission based) and/or customize the title/text of the purchase/purchase refund/renewal/renewal refund notifications title/text.
- Payment data tab - Allows the seller to configure his paypal address (custom paypal solution) or his payment profiles (xF payment profile solution).
- **[NEW 5.1.0]** Discounts tab - Allows the seller to manage his products' discounts.
- Sales tab - Shows all the sales you have done, ordered by latest ones with capability to filter them per user and/or per resource and/or per sales type (all/purchase/renewal) and/or purchase status **[NEW 5.1.0]** and/or per shipment status and/or per date **[NEW 5.1.0]**. From this page you can manually delete purchases or validate a pending purchase as well as export a sales log in .xlsx or csv format **[NEW 5.1.0]**.
- Products tab - Shows all the products you have for sale on the forum
- Licences tab - View all the licenses for your digital products with the capability to filter them per user and/or per resource and/or per license status (all/active/expired) in order to edit them or transfer license from an user to another
- For user with the right to, capability to configure the dashboard to show only information about own products or all thanks to a simple toggle control
- Last sales/Top sales widgets configured by default to display on that page.

## Member stats

- Most sales
- Most purchases
- Highest total sales amount

## User criteria

- Purchases
- Sales
- Total sales amount

## Fully configurable through options

- Extensively configurable through clean tabbed layout options list
- General options
  - Grid view layout activation on all pages/index
  - Number of purchases/licenses per page
  - Minimum resource price
  - Percentage on sales (if configured globally)
  - Definition of usergroup to which move users on purchase
- Payment
  - Payment processing method selection (Custom Paypal solution/xF payment profiles)
  - Custom paypal solution method configuration
    - Testing mode activation
    - Paypal address for categories using global payment configuration or for percentage on sale if configured globally
  - xF payment profiles method configuration
    - Payment profiles for categories using global payment configuration
    - Authorized payment providers solution
    - **[5.1.0]** Unpaid monthly invoices delay after which seller's sales are put on hold
  - **[5.1.0]** Unpaid purchases automatic pruning delay
- Licenses
  - Domain verification method selection and blacklist for digital products
  - License expiration alert mean selection (alert/email/both/none)
- Invoicing
  - Invoicing system activation
  - Invoices language selection
  - Invoice date/time format
- Statistics
  - Default currency
  - Default stats type
  - Display of purchases/sales/sales amount in user profile/member card
- Resources featuring
  - Purchase currency
  - Selection to moderate all resource featuring payments
- Resource prefixes
  - Prefix selection for digital/physical/service resources
  - Prefix selection for out-of-stock resources

## Extensive set of permissions

- General permissions
  - Is a seller
  - **[5.1.0]** Configure buyers notification means
  - **[5.1.0]** Customize buyers notifications content
- General moderator permissions
  - View all sales
  - Manage all licenses
- Resource permissions
  - Buy resources
  - Buy for a friend (digital products)
  - Download all (digital products)
  - Sell resources
  - Maximum number of resources for sale
  - Accept other payment means (manual agreement)
  - Bypass percentage on sale
  - Buy featuring
- Resource moderator permissions
  - Edit any sale
  - View all purchases log
