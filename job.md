# Niceloop_job
> job in niceloop pos

`* = required`

### jobs
| Name | Type | Description
| ----|----|-----------    
jobs | array of string | 'jobId1 , jobId2 ,jobId3 , ...'

### job
| Name | Type | Description
| ----|----|-----------   
customerId | string | รหัสลูกค้า
timestamp | string | เวลาลงบันทึก 
note | string| บันทึกเพิ่มเติม
table | string | โต๊ะลูกค้า
toKitchen | boolean | send job to printer     
device | string| เครื่องที่ใช้ในการสั่ง
items | [{object}](job.md#items) | item menu

### items
| Name | Type | Description
| ----|----|-----------  
node | [array object](job.md#item)  | item menu

### Item
| Name | Type | Description
| ----|----|-----------  
uuid\* | string   | รหัสสินค้า    
name | string | ชื่อสินค้า
qty | number | จำนวนสินค้า
unitPrice | number | n/a
extendedPrice | number | n/a
discount | number | ส่วนลด
discountedPrice | number| ส่วนลด
comment | string | คอมเม้น
toppings | [array object](job.md#topping) | ออฟชั่นเพิ่มเติมของอาหาร

### topping
| Name | Type | Description
| ----|----|-----------  
uuid\* | string | รหัสสินค้า
qty | number | จำนวนสินค้า
unitPrice | number | n/a
extendedPrice | number| n/a
discount | number | ส่วนลด
discountedPrice | number | ส่วนลด