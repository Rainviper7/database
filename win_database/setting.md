# setting
>setting (ตั้งค่า)

`* = required`
   
| Name | Type | Description
| ----|----|-----------  
addOn | object array | รายการ addOn ที่กำลัง active `[3Ml3kKEE,4J7JWDCa]`
member | [{member}](setting.md#member) |  ข้อมูล member
option | [{option}](setting.md#option) |  option ต่าง ๆ
paymentType | [{paymentType}](setting.md#paymenttype_uuid) |   รูปแบการชำระเงิน
printerSetting | [{printerSetting}](setting.md#printersetting) |  ตั้งค่าปริ๊นเตอร์
quickPayment | [{quickPayment_uuid}](setting.md#quickpayment_uuid)  |  quickPayment
receipt | [{receipt}](setting.md#receipt) | ใบเสร็จ?
tables | object |  โต๊ะ `A : 20,` //Zone มี โต๊ะ 20 โต๊ะ
timer | [{timer_uuid}](setting.md#timer_uuid) | จำกัดเวลารับประทานอาหาร 

#### member
| Name | Type | Description
| ----|----|-----------  
moneyToPoint | number |  ตัวแปรเอาไว้คำนวนหลังจากซื้อของเช่น สั่ง สั่งอาหาร 100 บาท ได้ 10 points
pointsToMoney | number |  pointsToMoney

#### option
| Name | Type | Description
| ----|----|-----------  
address | string | ที่อยู่  `address : home`
openCafeTime | number |  เลือกเวลาเปิดปิดร้าน
serviceCharge | number |  ...
shopName | string | ชื่อร้าน `shopname : Niceloop` 
tel | sting | `0925684445`

#### paymentType_uuid
| Name | Type | Description
| ----|----|-----------  
is_creditcard | boolean | เป็น credit card ?
is_entertain | boolean | entertain ?
name | string | `Master Card`
row | number | หมายเลขแถวแสดงผล

#### printerSetting
| Name | Type | Description
| ----|----|-----------  
printComment | boolean | ปริ๊น comment ?
printMoveTable | boolean | ปริ๊น ประวัติกายย้ายโต๊ะ ?
printOpenMenuReport | number | จำนวนการปริ๊น
printProductReport | number |  3
printSummaryReport | number |  4
printVoidItemsReport | number | 2

#### quickPayment_uuid
| Name | Type | Description
| ----|----|-----------               
color | number |  0, //เลือกสี
row | number | หมายเลขแถวแสดงผล
type | number | `0 = Bill, 1 = Coin`
url | string | `www.google.com`
value | number |  100

#### receipt
| Name | Type | Description
| ----|----|-----------  
footer | string | footer1, //Footer
header1 | string | ใบเสร็จ Order อาหาร, //Header 1
header2 | string | ...
printCopy | number | ปริ๊น coppy กี่ใบ
printReceiptAfterPayment | boolean |  `true`
shopName | string | `Niceloop`
showDateTime | number | `0 = date-time,1 = date,2 = none`

#### timer_uuid
| Name | Type | Description
| ----|----|-----------  
length | number |  ระยะเวลา `11`
message | string | `599 Premium Package`
row | number | หมายเลขแถวแสดงผล