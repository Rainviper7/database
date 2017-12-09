# Niceloop_receipt
> receipt bill in niceloop pos

`* = required`

### receipt 

| Name | Type | Description
| ----|----|-----------
| receipt | object | receipt bill
> properties

| Name | Type | Description
| ----|----|-----------
| id\* | string | firestore auto gen id  
| customerId | string | accountที่ใช้งาน          
| posId  | string  | เครื่องposที่ใช้งาน   
| hqId | string  | id ของ accountสาขาแม่
| datetime | datetime | วันที่เวลาทำการบันทึก
| shift| string | กะ/เวณ ที่เข้าทำงาน
| user | string | ชื่อพนักงานที่ใช้งานอยู่        
| note | string | บันทึกเพิ่มเติม
| billId | string | เลขที่บิล 
| isDeleted  | boolean | สถานะการลบรายการ
| deleteRemark | boolean| สถานะการลบบันทึกเพิ่มเติม 
| table | string| หมายเลขโต๊ะ
| [addOn](README_receipt.md#addon) | Object| ...

### customer
| Name | Type | Description
| ----|----|-----------
| guest   | number  | จำนวนลูกค้า  
| openTime  | datetime | เวลาเปิดร้าน    

###items
| Name | Type | Description
| ----|----|-----------
| [items](README_receipt.md#baseitem) | array object | สินค้า 

###tags
| Name | Type | Description
| ----|----|-----------
| tags  | object| แท็ก 
> properties 

| Name | Type | Description
| ----|----|----------- 
| name | boolean | สถานะชื่อ 

### money
| Name | Type | Description
| ----|----|-----------
| subTotal | number | ราคาสินค้าจริง ยังไม่ลดตัวสินค้า 
| discountItems | number  |  ลดราคาสินค้า
beforeVat | number| ราคาก่อนคิดภาษี      
vat | number | ค่าภาษี      
grandTotal  | number| ยอดสุทธิ     
rounding | number| rounding     
afterRounding | number| after rounding      
cost | number  | ต้นทุน

 ### payment
| Name | Type | Description
| ----|----|-----------       
payment | array object | รายการชำระเงิน
> properties

| Name | Type | Description
| ----|----|-----------     
name | string | ประเภทการชำระเงิน
[amount](README_receipt.md#reference) | number | ...

###  addOn 
| Name | Type | Description
| ----|----|----------- 
addOn| object | ...
> properties

| Name | Type | Description
| ----|----|-----------  
name\* | string | ชื่อสมมนาคุณ
uuid | string | รหัส
computeMode | number | `0 = on subTotal,  1 = on totalAfterItemDiscounted,2 = on accumulation`
mode | number|   0 input,   1 amount
modeValue | number | ค่าของmode 10percent   or   10 baht.
amount | number | '#/components/schemas/amount'

### member
| Name | Type | Description
| ----|----|-----------    
memberId\*  | string| idของสมาชิก
point | number | แต้มสะสม

### jobs
| Name | Type | Description
| ----|----|-----------    
jobs | array object | 'jobId1 , jobId2 ,jobId3 , ...'

### job
| Name | Type | Description
| ----|----|-----------   
 job | object | Jobs  Real time database
 > properties

| Name | Type | Description
| ----|----|-----------   
[customerId](README_receipt.md#reference) |  object | ...
[timestamp](README_receipt.md#reference) |  object | ...
note | string| บันทึกเพิ่มเติม
[table](README_receipt.md#reference) | object | ...
toKitchen | boolean | send job to printer     
device | string| เครื่องที่ใช้ในการสั่ง

### employee
| Name | Type | Description
employee| object | ลูกจ้างที่กดสั่ง
 > properties

| Name | Type | Description
| ----|----|-----------        
name | string| ชื่อลูกจ้าง
id | string| รหัสลูกจ้าง

| Name | Type | Description
| ----|----|-----------      
items | object | เมนู
 > properties

| Name | Type | Description
| ----|----|-----------  
[node](README_receipt.md#items) | object | ...

### infoRoot
 | Name | Type | Description
| ----|----|-----------  
infoRoot | object |   '{   "A1" :  {*info object *}    }'
 > properties

| Name | Type | Description
| ----|----|-----------  
[table](README_receipt.md#reference) |  object | ...
[info](README_receipt.md#infoobject) |  object | ...
             
### InfoObject
| Name | Type | Description
| ----|----|----------- 
 infoObject| object | ...
> properties

| Name | Type | Description
| ----|----|-----------  
isLock | boolean |  โตีะถูกล็อกมั้ย     
guest | number| จำนวนลูกค้า          
comment | array object |  " ['string', ...]"

### member
 | Name | Type | Description
| ----|----|----------- 
member | object | ...
> properties

| Name | Type | Description
| ----|----|-----------  
id\* | string |  id สมาชิก             
name | string |  ชื่อสมาชิก             
openTime | string |  เวลาเปิด??
noOfPrintPreview | number |  จำนวนสั่งปริ้นพรีวิว
[addOn](README_receipt.md#addon) | array object |  ส่วนเพิ่มเติม

 ### vat_obj                 
| Name | Type | Description
| ----|----|-----------             
vat_obj| object |  ภาษี  
> properties

| Name | Type | Description
| ----|----|-----------   
mode  | string |  โหมด
modeValue  | string |  ค่า
             
### RunningMode 
| Name | Type | Description
| ----|----|-----------   
runningMode| object | runningMode realtime database
> properties

| Name | Type | Description
| ----|----|-----------  
[shift](README_receipt.md#reference) | object | ...
[businessDay](README_receipt.md#reference) | object | ...
currentIdBill | string | idบิลปัจจุบัน
[currentEmployee](README_receipt.md#reference) |  object | ' people from WIN'
cashierMode | string | '0= cashier, 1= termial, 2= 2nd cashier'

### VoidItems
| Name | Type | Description
| ----|----|----------- 
voidItems| object |  VoidItems   Firestore
> properties

| Name | Type | Description
| ----|----|----------- 
id\* | string |  firebase store auto gen    
[businessDay](README_receipt.md#reference) |  object | ...
[customerId](README_receipt.md#reference) |  object | ...
uuid | string | item uuid
[datetime](README_receipt.md#reference) | object | ...
name | string |  ชื่อสินค้า
qty | number |  จำนวนสินค้า
price | number |  ราคาสินค้า
[table](README_receipt.md#reference) |  object | ...
reason | string |  คอมเม้นท์
        
          
### Acticity
| Name | Type | Description
| ----|----|----------- 
acticity | object | Acticity   Firestore
> properties

| Name | Type | Description
| ----|----|----------- 
[[timestamp](README_receipt.md#reference) | object | ...
table](README_receipt.md#reference) |  object | ...
type | string  |  ประเภทงาน
message | string |  ข้อความ          
ref | string |  'for reference to _id for job'
[customerId](README_receipt.md#reference) | object | ...
action | number | 'codeInt ex. 200 = add, 300 = move'          
[amount](README_receipt.md#reference) |  object | ...
employeeName | string |  ชื่อลูกจ้าง          
employeeId | string |  รหัสลูกจ้าง
          
          
### DrawerLogs
| Name | Type | Description
| ----|----|----------- 
drawerLogs | object | DrawerLogs Firestore
> properties

| Name | Type | Description
| ----|----|----------- 
[customerId](README_receipt.md#reference) | object | ...
[businessDay](README_receipt.md#reference)| object | ...
start | number |  เงินที่ใส่ในลิ้นชัก
pos | number |  ยอดขายจากระบบ  cash only
posEnding | number |  เงิน A
actualEnding | number |  เงิน B
diff | number |    'ส่วนต่างเงินในลิ้นชัก  A-B    |  ถ้าบวก เงินในระบบ เยอะกว่านับจริง  (เงินในลิ้นชักหาย) |  ถ้าลบ   เงินในลิ้นชักเยอะกว่าที่คำนวนได้ในระบบ ( เงินได้รับเกิน)'
    
| Name | Type | Description
| ----|----|-----------    
withdraw | array object |  '...'
> properties

| Name | Type | Description
| ----|----|----------- 
type | string |  'add | withdraw'               
[timestamp](README_receipt.md#reference) |  object | ...
[amount](README_receipt.md#reference) | object | ...
remark | string |  คอมเม้นต์
                

## Reference

| Name | Type | Description
| ----|----|-----------           
customerId | string | รหัสลูกค้า
timestamp | string | เวลาลงบันทึก   
table | string | โต๊ะลูกค้า
businessDay | string | วัน???  
datetime| string | วันที่เวลาทำการบันทึก
shift | string | กะ/เวณ ที่เข้าทำงาน
amount | number | 1500, -1500 ใส่เลข ลบถ้าหักออก
      
| Name | Type | Description
| ----|----|----------- 
employeeObj | object
> properties

| Name | Type | Description
| ----|----|----------- 
ex1| string | `...`

### baseItem
| Name | Type | Description
| ----|----|-----------
| baseItem  | object| ... 
> properties 

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
[toppings](README_receipt.md#topping) | array object | ออฟชั่นเพิ่มเติมของอาหาร

### topping
| Name | Type | Description
| ----|----|----------- 
topping| object | ...
> properties

| Name | Type | Description
| ----|----|-----------  
uuid\* | string | รหัสสินค้า
qty | number | จำนวนสินค้า
unitPrice | number | n/a
extendedPrice | number| n/a
discount | number | ส่วนลด
discountedPrice | number | ส่วนลด

### discount
| Name | Type | Description
| ----|----|-----------  
[discountAll1](README_receipt.md#discountall) | array object | ส่วนลดทั้งบิล
[discountAll2](README_receipt.md#discountall) | array object | ส่วนลดทั้งบิล2

### discountAll
| Name | Type | Description
| ----|----|-----------  
discountAll | object| ส่วนลดทั้งบิล   
> properties

| Name | Type | Description
| ----|----|-----------  
name | string | ชื่อส่วนลด          
[amount](README_receipt.md#discountall)|  object | ...
mode | number | โหมดส่วนลด  0 = ลดเป็นเปอเซ็นต์,   1 = discount amount          
modeValue | number | 'ค่าที่ต้องการทำส่วน mode|0 =10%, mode|1  =10 บาท'
            
