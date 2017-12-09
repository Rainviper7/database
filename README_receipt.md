# Niceloop_receipt
> receipt bill in niceloop pos

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
| note | string| บันทึกเพิ่มเติม
| billId | string| เลขที่บิล 
| isDeleted  | boolean| สถานะการลบรายการ
| deleteRemark | boolean| สถานะการลบบันทึกเพิ่มเติม 
| table | string| หมายเลขโต๊ะ
|addOn|Object|'#/components/schemas/addOn'

| Name | Type | Description
| ----|----|-----------
| guest   | number  | จำนวนลูกค้า  
| openTime  | datetime | เวลาเปิดร้าน    
| items | array object | สินค้า '#/components/schemas/baseItem' 
| subTotal | number | ราคาสินค้าจริง ยังไม่ลดตัวสินค้า 
| discountItems | number  |  ลดราคาสินค้า
| tags  | object| แท็ก 
> properties 
| Name | Type | Description
| ----|----|----------- 
| name | boolean | สถานะชื่อ 


| Name | Type | Description
| ----|----|----------- 
beforeVat | number| ราคาก่อนคิดภาษี      
vat | number | ค่าภาษี      
grandTotal  | number| ยอดสุทธิ     
rounding | number| rounding     
afterRounding | number| after rounding      
cost | number  | ต้นทุน

 ### payment
| Name | Type | Description
| ----|----|-----------       
payment | array obj | รายการชำระเงิน
> properties

| Name | Type | Description
| ----|----|-----------     
name | string | ประเภทการชำระเงิน
amount |number| '#/components/schemas/amount'

### member
 | Name | Type | Description
| ----|----|-----------    
memberId  | string| idของสมาชิก
point | number| แต้มสะสม

### jobs
| Name | Type | Description
| ----|----|-----------    
jobs | array obj |'jobId1 , jobId2 ,jobId3 , ...'
> properties

| Name | Type | Description
| ----|----|-----------  
... | string |'jobId1 , jobId2 ,jobId3 , ...'

### job
| Name | Type | Description
| ----|----|-----------   
 job | object | Jobs  Real time database
 > properties

| Name | Type | Description
| ----|----|-----------   
customerId | $ref | '#/components/schemas/customerId'
timestamp | $ref | '#/components/schemas/timestamp'
note | string| บันทึกเพิ่มเติม
table |$ref | '#/components/schemas/table'
employee| object | ลูกจ้างที่กดสั่ง
 > properties
| Name | Type | Description
| ----|----|-----------        
name | string| ชื่อลูกจ้าง
id | string| รหัสลูกจ้าง

| Name | Type | Description
| ----|----|-----------  
toKitchen | boolean | send job to printer     
device | string| เครื่องที่ใช้ในการสั่ง  

| Name | Type | Description
| ----|----|-----------      
items | object |เมนู
 > properties

| Name | Type | Description
| ----|----|-----------  
node | $ref| '#/components/schemas/items'


### infoRoot
 | Name | Type | Description
| ----|----|-----------  
infoRoot | object |   '{   "A1" |   {*info object *}    }'
 > properties

 | Name | Type | Description
| ----|----|-----------  
table | $ref | '#/components/schemas/table'
info | $ref | '#/components/schemas/infoObject'

             
### InfoObject  Real time database
| Name | Type | Description
| ----|----|----------- 
 infoObject| object |
> properties

 | Name | Type | Description
| ----|----|-----------  
isLock | boolean |  โตีะถูกล็อกมั้ย     
guest | number| จำนวนลูกค้า          
comment | array obj|  คอมเม้นต์
| ----|----|-----------           
items| string |" ['string', ...]"
| ----|----|-----------  

### member
 | Name | Type | Description
| ----|----|----------- 
member | object
> properties

| Name | Type | Description
| ----|----|-----------  
id | string |  id สมาชิก             
name | string |  ชื่อสมาชิก             
openTime | string|  เวลาเปิด??
noOfPrintPreview | number |  จำนวนสั่งปริ้นพรีวิว
addOn | array object |  ส่วนเพิ่มเติม '#/components/schemas/addOn'   

 ### vat_obj                 
| Name | Type | Description
| ----|----|-----------             
vat_obj| object|  ภาษี  
> properties

| Name | Type | Description
| ----|----|-----------   
mode  | string |  โหมด
modeValue  | string |  ค่า
             
### RunningMode 
| Name | Type | Description
| ----|----|-----------   
runningMode| object | realtime database
> properties

| Name | Type | Description
| ----|----|-----------  
shift |$ref| '#/components/schemas/shift'
businessDay |$ref| '#/components/schemas/businessDay'
currentIdBill | string | idบิลปัจจุบัน
currentEmployee | $ref | ' people from WIN' '#/components/schemas/employeeObj'
cashierMode | string | '0= cashier, 1= termial, 2= 2nd cashier'

### VoidItems
| Name | Type | Description
| ----|----|----------- 
    voidItems| object |  VoidItems   Firestore
> properties

| Name | Type | Description
| ----|----|----------- 
id| string |  firebase store auto gen    
businessDay | $ref | '#/components/schemas/businessDay'
customerId | $ref | '#/components/schemas/customerId'
uuid | string    | item uuid
datetime |$ref| '#/components/schemas/datetime'
name | string |  ชื่อสินค้า
qty | number|  จำนวนสินค้า
price | number|  ราคาสินค้า
table | $ref| '#/components/schemas/table'
reason | string|  คอมเม้นท์
        
          
### Acticity   Firestore
| Name | Type | Description
| ----|----|----------- 
acticity| object
> properties

| Name | Type | Description
| ----|----|----------- 
timestamp |$ref| '#/components/schemas/timestamp'
table | $ref| '#/components/schemas/table'
type | string  |  ประเภทงาน
message | string |  ข้อความ          
ref | string |  'for reference to _id for job'
customerId |$ref| '#/components/schemas/customerId'
action | number | 'codeInt ex. 200 = add, 300 = move'          
amount | $ref| '#/components/schemas/amount'
employeeName | string |  ชื่อลูกจ้าง          
employeeId | string|  รหัสลูกจ้าง
          
          
### DrawerLogs
| Name | Type | Description
| ----|----|----------- 
drawerLogs | object | DrawerLogs Firestore
> properties

| Name | Type | Description
| ----|----|----------- 
customerId|  $ref| '#/components/schemas/customerId'
businessDay | $ref| '#/components/schemas/businessDay'
start | number |  เงินที่ใส่ในลิ้นชัก
pos | number |  ยอดขายจากระบบ  cash only
posEnding | number  |  เงิน A
actualEnding | number |  เงิน B
diff | number|    'ส่วนต่างเงินในลิ้นชัก  A-B    |  ถ้าบวก เงินในระบบ เยอะกว่านับจริง  (เงินในลิ้นชักหาย) |  ถ้าลบ   เงินในลิ้นชักเยอะกว่าที่คำนวนได้ในระบบ ( เงินได้รับเกิน)'
    
| Name | Type | Description
| ----|----|-----------    
withdraw | array object |  '...'
> properties

| Name | Type | Description
| ----|----|----------- 
type | string |  'add | withdraw'               
timestamp | $ref | '#/components/schemas/timestamp'
amount |$ref | '#/components/schemas/amount'
remark | string |  คอมเม้นต์
                

## Referrence
| Name | Type | Description
| ----|----|----------- 
employeeObj| object
> properties

| Name | Type | Description
| ----|----|----------- 
ex1| string | `...`

| Name | Type | Description
| ----|----|-----------           
customerId | string| รหัสลูกค้า
timestamp | string| เวลาลงบันทึก   
table | string| โต๊ะลูกค้า
businessDay | string | วัน???  
datetime| string| วันที่เวลาทำการบันทึก
shift | string| กะ/เวณ ที่เข้าทำงาน
amount | number | 1500, -1500 ใส่เลข ลบถ้าหักออก
      

### baseItem
| Name | Type | Description
| ----|----|-----------  
uuid\* | string   | รหัสสินค้า    
name | string| ชื่อสินค้า
qty | number| จำนวนสินค้า
unitPrice| number | n/a
extendedPrice | number | n/a
discount | number| ส่วนลด
discountedPrice| number| ส่วนลด
comment | string| คอมเม้น
toppings | array object | ออฟชั่นเพิ่มเติมของอาหาร '#/components/schemas/topping'

### topping
| Name | Type | Description
| ----|----|----------- 
topping| object | ...
> properties

| Name | Type | Description
| ----|----|-----------  
uuid\* | string   | รหัสสินค้า
qty | number| จำนวนสินค้า
unitPrice | number| n/a
extendedPrice | number| n/a
discount | number| ส่วนลด
discountedPrice| number| ส่วนลด

###  addOn 
| Name | Type | Description
| ----|----|----------- 
addOn| object | ...
> properties

| Name | Type | Description
| ----|----|-----------  
name\* | string | ชื่อสมมนาคุณ
uuid | string| รหัส
computeMode | number | `0 = on subTotal,  1 = on totalAfterItemDiscounted,2 = on accumulation`
mode | number|   0 input,   1 amount
modeValue | number | ค่าของmode 10percent   or   10 baht.
amount | number | '#/components/schemas/amount'


discountAll1 | array object  | ส่วนลดทั้งบิล '#/components/schemas/discountAll'
discountAll2 | array object  | ส่วนลดทั้งบิล2 '#/components/schemas/discountAll'

discountAll | object| ส่วนลดทั้งบิล   
> properties|
        name | string | ชื่อส่วนลด          
        amount | $ref | '#/components/schemas/amount'
        mode | number | โหมดส่วนลด  0 = ลดเป็นเปอเซ็นต์,   1 = discount amount          
        modeValue | number | 'ค่าที่ต้องการทำส่วน mode|0 =10%, mode|1  =10 บาท'
            