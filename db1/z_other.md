### tags
| Name | Type | Description
| ----|----|----------- 
| name | boolean | สถานะชื่อ

### vat_obj                 
| Name | Type | Description
| ----|----|-----------   
mode | string |  โหมด
modeValue | string |  ค่า
             
### VoidItems
| Name | Type | Description
| ----|----|----------- 
id\* | string |  firebase store auto gen    
businessDay | string | วัน???  
customerId | string | รหัสลูกค้า
uuid | string | item uuid
datetime| string | วันที่เวลาทำการบันทึก
name | string | ชื่อสินค้า
qty | number | จำนวนสินค้า
price | number |  ราคาสินค้า
table | string | โต๊ะลูกค้า
reason | string |  คอมเม้นท์
             
### Acticity
| Name | Type | Description
| ----|----|----------- 
timestamp | string | เวลาลงบันทึก 
table | string | โต๊ะลูกค้า
type | string |  ประเภทงาน
message | string |  ข้อความ          
ref | string |  'for reference to _id for job'
customerId | string | รหัสลูกค้า
action | number | 'codeInt ex. 200 = add, 300 = move'          
amount | number | ค่าเงิน 1500, -1500 ใส่เลข ลบถ้าหักออก
employeeName | string |  ชื่อลูกจ้าง          
employeeId | string |  รหัสลูกจ้าง
                       
### employeeObj\not complete
| Name | Type | Description
| ----|----|----------- 
ex1| string | `...`