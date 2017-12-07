# Niceloop_receipt
> receipt bill in niceloop pos

### receipt 
| Name | Type | Description
| ----|----|-----------
| id | string | firestore auto gen id  
| customerId | string | accountที่ใช้งาน          
| posId  | string  | เครื่องposที่ใช้งาน   
| hqId | string  | id ของ accountสาขาแม่
| datetime | datetime | วันที่เวลาทำการบันทึก
| shift| string | กะ/เวณ ที่เข้าทำงาน
| user | string | ชื่อพนักงานที่ใช้งานอยู่        
| note | string| บันทึกเพิ่มเติม
| billId | string| เลขที่บิล 
| isDeleted  | boolean| สถานะการลบรายการ
| deleteRemark | boolean| สถานะการลบบันทึกเพิ่มเติม 
| table | string| หมายเลขโต๊ะ

## customer

### guest
| Name | Type | Description
| ----|----|-----------
| guest   | number  | จำนวนลูกค้า  

### openTime
 | Name | Type | Description
| ----|----|-----------
| openTime  | datetime | เวลาเปิดร้าน

### items
| Name | Type | Description
| ----|----|-----------       
| items | array of | สินค้า '#/components/schemas/baseItem' 

### tags
| Name | Type | Description
| ----|----|-----------         
| tags  | object| แท็ก
     
#### tags
>tags

| Name | Type | Description
| ----|----|-----------       
| name | boolean | สถานะชื่อ

### baseItem
| Name | Type | Description
| ----|----|-----------  
uuid | string   | รหัสสินค้า    
name | string| ชื่อสินค้า
qty | number| จำนวนสินค้า
unitPrice| number | n/a
extendedPrice | number | n/a
discount | number| ส่วนลด
discountedPrice| number| ส่วนลด
comment | string| คอมเม้น
toppings | array of | ออฟชั่นเพิ่มเติมของอาหาร '#/components/schemas/topping'

 ## money all decimal

 ### subTotal
| Name | Type | Description
| ----|----|-----------  
subTotal | number | ราคาสินค้าจริง ยังไม่ลดตัวสินค้า

### discountItems
| Name | Type | Description
| ----|----|-----------  
discountItems | number  |  ลดราคาสินค้า
               