================
Product variants
================

Product variants are used to manage products with different variations, such as size, color, etc.
They can be used to manage the product at the template level, which will be for all variations,
and/or at the variant level, which is for specific attributes.

As an example, a company selling t-shirts may have the following
product:


- T-shirt

  - Sizes: S, M, L, XL, XXL
  - Colors: Blue, Red, White, Black

In this example, the **T-Shirt** is the product template and
**T-Shirt, S, Blue** is a product variant. Sizes and color are
**attributes**.

The above example has a total of 20 different products (5 sizes x 4
colors). Each one of these products has its own inventory, sales, etc.

Impact of variants
==================

- **Barcode**: The code and barcode are associated with each variant instead of per template.
  Each individual variant can have its own unique barcode / SKU.

- **Price**: Every product variant has its own public price, which is the sum of the template
  price and any optional charges for particular variants. For example, a red shirt’s cost is $23
  because the shirt’s template price is $20 and an additional $3 for the red color variant.
  Pricelist rules can be defined to apply on the template or the variant pricing.

- **Inventory**: Inventory is managed based upon product variants. You don't own just t-shirts,
  but instead, you own Red, Size Small T-shirts or Blue, Size Medium T-shirts. On the product
  template form, the inventory shows the sum of all variants, but the actual inventory is computed
  by individual variants.

- **Picture**: Every product variation can have its own primary picture.

- **Other fields**: Many fields belong specifically to the product template. Updating these
  fields automatically updates every variant as well. Examples include Income Account and Taxes.

Configuring Variants
====================

Activating the variant feature
------------------------------

Before using product variants, the setting needs to be activated. To do so, you must go to the
Sales app. Select :menuselection:`Configuration --> Settings`, locate the **Products Variants**
line via scrolling or the search bar at the top of the page.

.. image:: variants/activating-variants-setting.png
   :align: center
   :alt: Activating Product Variants settings

Creating Attributes
-------------------

Attributes need to be created before product variants can be set up in your database. Attributes
can be accessed via :menuselection:`Configuration --> Attributes`. To create a new Attribute,
click **Create**. First, choose an attribute name, such as “color” or “size.”

Then, select a display type from Radio, Select, and Color, which determines how your product will
be shown on your eCommerce page, PoS dashboard or Product Configurator. Radio lists your options
in a bullet style list; Select creates a dropdown menu; and Color creates little squares to
choose the options from.

.. image:: variants/display-types-configurator.png
   :align: center
   :alt: Display Types on Product Configurator

Selecting a Variants Creation Mode informs Odoo when a new variant needs to be created once an
attribute is added to a product. The available options are instantly, dynamically, or never.
Instantly will create all possible variants as soon as an attribute and values are added to a
product. Dynamically will create variants only when corresponding attributes and values are added
to a sales order. Never as a selection means that variants are never created a particular attribute.

.. note::
   Once added to a product, an attribute’s Variants Creation Mode cannot be edited.

Values should be added to an attribute before saving, but more values can be added at any time,
if needed. To add a value, click **Add a Line.** From there, you can:

#. type in the value’s name
#. check whether or not the value is custom
#. specifically for colors, add an html color code to make it even easier for salespeople and
   customers to know what they’re selecting.

A color code can be selected by either dragging around the slider or entering a specific HTML
color code to ensure an exact product match whenever possible.

.. image:: variants/picking-a-color.png
   :align: center
   :alt: Selecting a Color

.. tip::
   **Attributes** can also be created on the fly by adding a new line and typing the name into the
   Variants Tab on a product.

A new tab appears on the attribute’s page called **Related Products** after an attribute is added
to a product. This tab lists every product in your database using the attribute.

Creating products with variants
-------------------------------

Head over to the Products page by clicking :menuselection:`Sales → Products --> Products`, and
then, either select a product to add variants to or create a new one by tapping **Create**.

On the product page, a new tab called Variants has appeared. The smart button at the top of the
template indicates the number of currently configured variants on this product.

.. image:: variants/variant-smart-button.png
   :align: center
   :alt: Variants smart button

To add a new variant, click on the **Variants Tab**, then on **Add Any Line** to add any
attributes and values to create new product options for your customers.

.. tip::
   The order of Attributes on the Attributes page dictates how they appear on the Product
   Configurator, PoS dashboard or eCommerce pages.

Similar creation processes are accessible through the Purchase, Inventory, and eCommerce
applications.

Managing product exclusions
---------------------------

The examples below are all based on this product template that has two variant attributes :

-  T-Shirt

   -  Color: Red, Blue, White

   -  Size: S, M, L, XL, XXL

With the above product template, you have 15 different t-shirt products in 3 different colors and
5 different sizes. If the red and blue t-shirts are the only shirts available in XXL, you can
deactivate the white variant.

Open :menuselection:`Sales --> Products` and select the product you want to edit. Click on the
**Configure Variants** button, select the line item for the White Color Attribute, and then click
on **Edit**. Click **Add a line** and select any product(s) and/or specific attribute values that
are incompatible with this color.

.. image:: variants/attribute-exclusions.png
   :align: center
   :alt: Excluding Attributes

Setting a price per variant
---------------------------

Extra costs can be added to the main price for specific product variants.

To add an extra cost to a specific variant, open :menuselection:`Sales --> Products`, and click
on the product you want to modify. Click on **Configure Variants** to access the list of variant
values.

Click on the variant you wish to add a value to bring up the template and click **Edit**. In the
**Value Price Extra** field, type in the cost value for the particular variant that is added to
the original price.

.. image:: variants/value-price-extra.png
   :align: center
   :alt: Value Price Extra

When you have entered all the extra values you need, click on **Save**.