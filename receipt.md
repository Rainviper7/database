# Niceloop_receipt
> receipt bill in niceloop pos

`* = required`

### receipt 
| Name | Type | Description
| ----|----|-----------
| id\* | string | firestore auto gen id  
| customerId | string | accountที่ใช้งาน          
| posId  | string  | เครื่องposที่ใช้งาน   
| hqId | string  | id ของ accountสาขาแม่
datetime| string | วันที่เวลาทำการบันทึก
shift | string | กะ/เวร ที่เข้าทำงาน
| user | string | ชื่อพนักงานที่ใช้งานอยู่        
| note | string | บันทึกเพิ่มเติม
| billId | string | เลขที่บิล 
| isDeleted  | boolean | สถานะการลบรายการ
| deleteRemark | boolean| สถานะการลบบันทึกเพิ่มเติม 
| table | string| หมายเลขโต๊ะลูกค้า
| addOn | [{object}](receipt.md#addon) | ...
| guest   | number  | จำนวนลูกค้า  
| openTime  | datetime | เวลาเปิดร้าน    
| items | [array object](receipt.md#item) | สินค้า 
| subTotal | number | ราคาสินค้าจริง ยังไม่ลดตัวสินค้า 
| discountItems | number  |  ลดราคาสินค้า
|beforeVat | number| ราคาก่อนคิดภาษี      
|vat | number | ค่าภาษี      
|grandTotal  | number| ยอดสุทธิ     
|rounding | number| rounding     
|afterRounding | number| after rounding      
|cost | number  | ต้นทุน

### payment
| Name | Type | Description
| ----|----|-----------     
name | string | ประเภทการชำระเงิน
amount | number | ค่าเงิน 1500, -1500 ใส่เลข ลบถ้าหักออก

### tags
| Name | Type | Description
| ----|----|----------- 
| name | boolean | สถานะชื่อ

### addOn 
| Name | Type | Description
| ----|----|-----------  
name\* | string | ชื่อสมมนาคุณ
uuid | string | รหัส
computeMode | number | `0 = on subTotal,  1 = on totalAfterItemDiscounted,2 = on accumulation`
mode | number|   0 input,   1 amount
modeValue | number | ค่าของmode 10percent   or   10 baht.
amount | number | ค่าเงิน 1500, -1500 ใส่เลข ลบถ้าหักออก

### member
| Name | Type | Description
| ----|----|-----------    
memberId\* | string | idของสมาชิก
name | string |  ชื่อสมาชิก   
point | number | แต้มสะสม

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
items | [{object}](receipt.md#items) | item menu

### items
| Name | Type | Description
| ----|----|-----------  
node | [array object](receipt.md#item)  | item menu

### employee
| Name | Type | Description
| ----|----|-----------        
name | string | ชื่อลูกจ้าง
id | string | รหัสลูกจ้าง

### infoRoot
| Name | Type | Description
| ----|----|-----------  
table | string | โต๊ะลูกค้า
info | [{object}] (receipt.md#infoobject) | ...
             
### InfoObject
| Name | Type | Description
| ----|----|-----------  
isLock | boolean |  โตีะถูกล็อกมั้ย     
guest | number| จำนวนลูกค้า          
comment | array of string |  " ['string', ...]"
member | [{object}](receipt.md#member)| ลูกค้าสมาชิก        
openTime | string |  เวลาเปิด??
noOfPrintPreview | number |  จำนวนสั่งปริ้นพรีวิว
addOn | [array object](receipt.md#addon) |  ส่วนเพิ่มเติม

### vat_obj                 
| Name | Type | Description
| ----|----|-----------   
mode | string |  โหมด
modeValue | string |  ค่า
             
### RunningMode 
| Name | Type | Description
| ----|----|-----------  
shift | string | กะ/เวร ที่เข้าทำงาน
businessDay | string | วัน???  
currentIdBill | string | idบิลปัจจุบัน
currentEmployee | [{object}](receipt.md#employeeobj) | ' people from WIN'
cashierMode | string | '0= cashier, 1= termial, 2= 2nd cashier'

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
                   
### DrawerLogs
| Name | Type | Description
| ----|----|----------- 
customerId | string | รหัสลูกค้า
businessDay | string | วัน???  
start | number |  เงินที่ใส่ในลิ้นชัก
pos | number |  ยอดขายจากระบบ  cash only
posEnding | number |  เงิน A
actualEnding | number |  เงิน B
diff | number |    'ส่วนต่างเงินในลิ้นชัก  A-B      ถ้าบวก เงินในระบบ เยอะกว่านับจริง  (เงินในลิ้นชักหาย)   ถ้าลบ   เงินในลิ้นชักเยอะกว่าที่คำนวนได้ในระบบ ( เงินได้รับเกิน)'
withdraw | [{array object}](receipt.md#withdraw) |  '...'

### withdraw
| Name | Type | Description
| ----|----|----------- 
type | string |  'add \| withdraw'               
timestamp | string | เวลาลงบันทึก 
amount | number | ค่าเงิน 1500, -1500 ใส่เลข ลบถ้าหักออก
remark | string |  คอมเม้นต์
      
### employeeObj\not complete
| Name | Type | Description
| ----|----|----------- 
ex1| string | `...`

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
toppings | [array object](receipt.md#topping) | ออฟชั่นเพิ่มเติมของอาหาร

### topping
| Name | Type | Description
| ----|----|-----------  
uuid\* | string | รหัสสินค้า
qty | number | จำนวนสินค้า
unitPrice | number | n/a
extendedPrice | number| n/a
discount | number | ส่วนลด
discountedPrice | number | ส่วนลด