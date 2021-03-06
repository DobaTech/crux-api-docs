---
title: Submitting Tracking Information
name:
position: 5
visibility: file-specs
method:
description: How do I submit tracking information
right_code: |
  ~~~ bash
  retailer_org_uuid
  retailer_po
  tracking_number
  sku_id
  ~~~
  {: title="Required Fields" }

  ~~~ bash
  quantity_shipped
  supplier_provided_sku_cost
  ~~~
  {: title="Preferred Fields" }

  ~~~ bash
  supplier_po
  supplier_provided_notes
  supplier_provided_order_attributes
  ~~~
  {: title="Desired Fields" }

---
----
### File Sample

* ***csv*** <a href="/files/file-samples/csv/tracking_sample.csv">Tracking Sample Download</a>
* ***xlsx*** <a href="/files/file-samples/xlsx/product_sample.xlsx">Tracking Sample Download</a>

----
### Submitting Files - FTP

#### File Details

##### Naming convention

tracking_date.csv
{: .info }
tracking_date.xlsx
{: .info }

- Acceptable characters, [A-Za-z0-9-_]
- Character encoding (UTF-8)
- Line Feed (\n) required
- Proper naming conventions. (file names must not include spaces)

#### FTP Upload
1.	Create your file based on our sample files and specs, including all required fields.
2.	Log into your Crux-provided FTP
3.	Upload file inside ***/in*** directory

----
### Submitting Tracking - Crux Website

1.	On the Dashboard, go to ***Orders Awaiting Tracking*** and click on the order you wish to allocate
  - or go to the ***Orders*** tab then ***Add tracking*** tab that will appear underneath to view any orders pending tracking.
2.	Click on the order you wish to add tracking to and select ***Add Tracking***. A sidebar will appear on the right.
3.	Enter tracking number under the box labeled ***Tracking Number***.
4.	Enter the amount of items included in your shipment under ***Items included***.
5.	Enter the cost of the shipment under ***Ship Cost***.
6.	Enter the carrier name under ***Carrier***.
7.	Enter the shipping method under ***Method***.
8.	Provide the weight of the package under ***Weight***.
9.	Submit by clicking ***Add tracking***.
10.	To export one or more orders into a spreadsheet, select the checkbox next to the order and click on the red ***Export*** button at the top.
