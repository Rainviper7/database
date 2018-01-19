### retail_department
> retail_department (หมวดหมู่ของ สินค้า retail)

| Name | Type | Description
| ----|----|-----------  
{departments_uuid6} | [{object}](z_part2.md#departments_uuid6) | uuid สาขาแม่ `3181`

#### departments_uuid6
| Name | Type | Description
| ----|----|-----------  
{retailDepartment_uuid} | [{object}](z_part2.md#retailDepartment_uuid) |  retailDepartment uuid

#### retailDepartment_uuid
| Name | Type | Description
| ----|----|-----------  
name | string | `สุขภัณต์`
row | number | หมายเลขแถวแสดงผล
uuid | string | `0y37Si1E`
    

### retail_groups
>retail_groups(กลุ่มของ สินค้า retail)

| Name | Type | Description
| ----|----|-----------  
{departments_uuid7} | [{object}](z_part2.md#departments_uuid7) | uuid สาขาแม่ `3181`

#### departments_uuid7
| Name | Type | Description
| ----|----|-----------  
{retailGroups_uuid} | [{object}](z_part2.md#retailGroups_uuid) | uuid `6mKQ8rTJ`

#### retailGroups_uuid
| Name | Type | Description
| ----|----|-----------   
department | string | uuid หมวดหมู่ของ สินค้า retail  `mD6BxNaH`
name | string | `แปรงสีฟัน`
row | number | หมายเลขแถวแสดงผล
uuid | string | `6mKQ8rTJ`          


### retail_products
>retail_products (สินค้า retail)

| Name | Type | Description
| ----|----|-----------  
{departments_uuid8} | [{object}](z_part2.md#departments_uuid8) | uuid สาขาแม่ `3181`

#### departments_uuid8
| Name | Type | Description
| ----|----|-----------  
{retailProducts_uuid} | [{object}](z_part2.md#retailProducts_uuid) | `09bxkhYx`

#### retailProducts_uuid
| Name | Type | Description
| ----|----|-----------  
barcode | string | `barcode : "f2f2"`
department | string | uuid หมวดหมู่ของ สินค้า retail `department : hcSUTVxI`
group | string | uuid กลุ่มของ สินค้า retail `TSvs2iLm`
name | string | `คอลเกต`
note | string | บันทึกข้อความ
price | number | ราคา `40`
productcode | string | รหัสสินค้า `"f23f2f2"`
row | number | หมายเลขแถวแสดงผล
unit | string | หน่วยนับ
uuid | string | `09bxkhYx`

### setting
>setting (ตั้งค่า)

| Name | Type | Description
| ----|----|-----------  
{departments_uuid9} | [{object}](z_part2.md#departments_uuid9) | uuid สาขาลูก `3180`

#### departments_uuid9      
| Name | Type | Description
| ----|----|-----------  
addOn | object array | รายการ addOn ที่กำลัง active `[3Ml3kKEE,4J7JWDCa]`
member | [{object}](z_part2.md#memberdepartments_uuid9) |  ข้อมูล member
option | [{object}](z_part2.md#optiondepartments_uuid9) |  option ต่าง ๆ
paymentType | [{object}](z_part2.md#paymentTypedepartments_uuid9) |   รูปแบการชำระเงิน
printerSetting | [{object}](z_part2.md#printerSettingdepartments_uuid9) |  ตั้งค่าปริ๊นเตอร์
quickPayment | [{object}](z_part2.md#quickPaymentdepartments_uuid9) |  quickPayment
receipt | [{object}](z_part2.md#receiptdepartments_uuid9) |  { ใบเสร็จ?
tables | object |  { โต๊ะ `A : 20,` //Zone มี โต๊ะ 20 โต๊ะ
timer | [{object}](z_part2.md#timerdepartments_uuid9) |  { จำกัดเวลารับประทานอาหาร

#### member(departments_uuid9)
| Name | Type | Description
| ----|----|-----------  
moneyToPoint | number |  ตัวแปรเอาไว้คำนวนหลังจากซื้อของเช่น สั่ง สั่งอาหาร 100 บาท ได้ 10 points
pointsToMoney | number |  ...

#### option(departments_uuid9)
| Name | Type | Description
| ----|----|-----------  
address | string | ที่อยู่  `address : home`
openCafeTime | number |  เลือกเวลาเปิดปิดร้าน
serviceCharge | number |  ...
shopName | string | ชื่อร้าน `shopname : Niceloop` 
tel | sting | `0925684445`

#### paymentType(departments_uuid9)
| Name | Type | Description
| ----|----|-----------  
{paymentType_uuid} | [{object}](z_part2.md#accounting) |  `-Kq295xokOGFie07QPQw`

#### paymentType_uuid
| Name | Type | Description
| ----|----|-----------  
is_creditcard | boolean | เป็น credit card ?
is_entertain | boolean | entertain ?
name | string | Master Card1,
row | number | หมายเลขแถวแสดงผล


#### printerSetting(departments_uuid9)
| Name | Type | Description
| ----|----|-----------  
printComment | boolean | ปริ๊น comment ?
printMoveTable | boolean | ปริ๊น ประวัติกายย้ายโต๊ะ ?
printOpenMenuReport | number | จำนวนการปริ๊น
printProductReport | number |  3
printSummaryReport | number |  4
printVoidItemsReport | number | 2

#### quickPayment(departments_uuid9)
| Name | Type | Description
| ----|----|-----------  
{quickPayment_uuid} | [{object}](z_part2.md#quickPayment_uuid) |  `fffqfqq`

#### quickPayment_uuid
| Name | Type | Description
| ----|----|-----------               
color | number |  0, //เลือกสี
row | number | หมายเลขแถวแสดงผล
type | number | `0 = Bill, 1 = Coin`
url | string | `www.google.com,`
value | number |  100

#### receipt(departments_uuid9)
| Name | Type | Description
| ----|----|-----------  
footer | string | footer1, //Footer
header1 | string | ใบเสร็จ Order อาหาร, //Header 1
header2 | string | ...
printCopy | number | ปริ๊น coppy กี่ใบ
printReceiptAfterPayment | boolean |  `true`
shopName | string | `Niceloop`
showDateTime | number | `0 = date-time,1 = date,2 = none`

#### timer(departments_uuid9)
| Name | Type | Description
| ----|----|-----------  
{timer_uuid} | [{object}](z_part2.md#timer_uuid) | `-Kr19eQwyGLP0WNBvI5r`

#### timer_uuid
| Name | Type | Description
| ----|----|-----------  
length | number |  ระยะเวลา `11`
message | string | `599 Premium Package`
row | number | หมายเลขแถวแสดงผล
            
### topping
| Name | Type | Description
| ----|----|-----------  
{departments_uuid10} | [{object}](z_part2.md#departments_uuid10) | uuid สาขาลูก `3180`

#### departments_uuid10
| Name | Type | Description
| ----|----|-----------  
{topping_uuid} | [{object}](z_part2.md#topping_uuid) |  uuid กลุ่มของ topping   `QV0dqh2r` 

#### topping_uuid
| Name | Type | Description
| ----|----|-----------  
items | [{object}](z_part2.md#itemstopping) | items ในกลุ่มของ topping
name | string | `Chips`
row | number | หมายเลขแถวแสดงผล
uuid |  | `QV0dqh2r`

#### items(Topping)
| Name | Type | Description
| ----|----|-----------  
 itemsTopping_uuid} | [{object}](z_part2.md#itemstopping_uuid) |   uuid items ในกลุ่มของ topping `kjBonvfw`

#### itemsTopping_uuid
name | string | `Lays`
price | number | ราคาท็อปปิ้ง
row | number | หมายเลขแถวแสดงผล
uuid | string | `kjBonvfw`

### user
| Name | Type | Description
| ----|----|-----------  
{user_uuid} | [{object}](z_part2.md#user_uuid) | uuid user    `A4hVJYUQrQfnzpfhmnii6S7td0m1`

#### user_uuid
| Name | Type | Description
| ----|----|-----------  
customerId | string |  `3180`
email | string | `3180@niceloop.com`
hqId | string | head quarter id (id ของสาขาแม่) `3181`
uuid | string | `A4hVJYUQrQfnzpfhmnii6S7td0m1`
