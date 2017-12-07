# Niceloop_receipt
> receipt bill in niceloop pos

### receipt 
| Name | Type | Description
| ----|----|-----------
| id | string | firestore auto gen id  
| customerId | string | accountที่ใช้งาน          
| posId  | string  | เครื่องposที่ใช้งาน   
| hqId | string  | id ของ accountสาขาแม่
| datetime | object_ref| วันที่เวลาทำการบันทึก
| shift| object_ref | กะ/เวณ ที่เข้าทำงาน
| user | string | ชื่อพนักงานที่ใช้งานอยู่        
| note | string| บันทึกเพิ่มเติม
| billId | string| เลขที่บิล 
| isDeleted  | boolean| สถานะการลบรายการ
| deleteRemark | boolean| สถานะการลบบันทึกเพิ่มเติม 
| table | string| หมายเลขโต๊ะ
          
