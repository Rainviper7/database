# branch_override (win\_db)
>branch_override คือข้อมูลของสาขาแม่ที่เอามาดัดแปลงประยุกต์ใช้กับสาขาลูก เช่น เมนูข้าวมันไก่ของสาขาแม่ 50 บาท แต่สาขาลูกอยากจะขายในราคา 60 บาทก็จะเกิิดการเปลี่ยนแปลงข้อมูลและนำข้อมูลที่เขียนทับมาไว้ใน branch_override

`* = required`

#### branchOverride_uuid
| Name | Type | Description
| ----|----|-----------  
accounting | [{accounting_uuid}](branch_override.md#accounting_uuid) | uuid
departmentGroups | [{departmentGroups_uuid}](branch_override.md#departmentgroups_uuid) | uuid
departments | [{departments_uuid}](branch_override.md#departments_uuid) | uuid ของรายการเมนูนั้น ๆ
promotion | [{promotion_key}](branch_override.md#promotion_key) | key ของ promotion นั้น ๆ
topping | [{topping_uuid}](branch_override.md#topping_uuid) | uuid ของ topping นั้น ๆ 

#### accounting_uuid
| Name | Type | Description
| ----|----|-----------  
uuid\* | string | รหัส?
computeMode | number| วิธีการคำนวน `0=คิดจากยอดsub total,1=คิดหลังจากหักลดสินค้าแล้ว,2=สะสมยอดแต่ละบรรทัด`
mode | number | `0= % , 1= Baht`
modeValue | number | จำนวนเงิน Baht หรือ %

#### departmentGroups_uuid            
| Name | Type | Description
| ----|----|-----------  
printer | {object boolean} | เลข printer ที่ active `3: true`

#### departments_uuid
| Name | Type | Description
| ----|----|-----------  
price | number | ราคา

#### promotion_key
| Name | Type | Description
| ----|----|-----------
isActive | boolean | กำลังเปิดใช้โปรโมชั่นนั้น ๆ อยู่หรือไม่

#### topping_uuid
| Name | Type | Description
| ----|----|-----------  
price | number | ราคาtopping