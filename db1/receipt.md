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
| addOn | [{addOn}](receipt.md#addon) | ...
| guest   | number  | จำนวนลูกค้า  
| openTime  | datetime | เวลาเปิดร้าน    
| items | [{item}](job.md#item) | สินค้า 
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

### addOn 
| Name | Type | Description
| ----|----|-----------  
name\* | string | ชื่อสมมนาคุณ
uuid | string | รหัส
computeMode | number | `0 = on subTotal,  1 = on totalAfterItemDiscounted,2 = on accumulation`
mode | number|   0 input,   1 amount
modeValue | number | ค่าของmode 10percent   or   10 baht.
amount | number | ค่าเงิน 1500, -1500 ใส่เลข ลบถ้าหักออก