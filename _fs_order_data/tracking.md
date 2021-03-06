---
title: Tracking
name:
position: 2
visibility: file-specs
method:
description: The Tracking section
right_code: |

---

retailer_org_uuid
: (string) ***Required*** Retailers Organization Universal Unique Identifier for the organization

retailer_po
: (string) ***Required*** Retailer provided purchase order number

tracking_number
: (string) ***Required*** Order tracking number

sku_id
: (string) ***Required*** The SKU Identifier for the SKU as provided by the Supplier

quantity_shipped
: (integer) ***Required*** Quantity shipped

supplier_provided_sku_cost
: (decimal) Supplier provided SKU cost (2 decimal places)

package_weight
: (string) The weight of the product when packaged for shipping

package_ship_date
: (string) Date that the packaged SKU will be available for shipment.

supplier_provided_method
: (string) Shipping method provided upon order.

supplier_provided_carrier
: (string) Shipping carrier provided upon order.

package_attributes
: (array) Package name and value attribute. (format: 'NAME':'VALUE';;'NAME':'VALUE')

supplier_po
: (string) ***Required*** The Purchase Order ID that you provide to identify your order

supplier_provided_notes
: (string) Supplier provided notes

supplier_provided_order_attributes
: (array) Array of supplier provided Order Attribute objects

supplier_provided_line_item_attributes
: (array) Array of supplier provided Line Item objects