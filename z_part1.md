# Niceloop_info
> infomation in niceloop pos

`* = required`

### infoRoot
| Name | Type | Description
| ----|----|-----------  
table | string | โต๊ะลูกค้า
info | [{object}](info.md#infoobject) | ...

### accounting
| Name | Type | Description
|----|----|-----------  
uuid\* | string | รหัส?
accountType | number | ชนิดของ account `0=assets,1=liability,2=equity,3=revennu 4=expence`
computeMode | number| วิธีการคำนวน `0=คิดจากยอดsub total,1=คิดหลังจากหักลดสินค้าแล้ว,2=สะสมยอดแต่ละบรรทัด`
mode | number | `0= % , 1= Baht`
modeValue | number | จำนวนเงิน Baht หรือ %
name | stirng | Discount Voucher
row | number | หมายเลขแถวแสดงผล

### branch_override
>branch_override คือข้อมูลของสาขาแม่ที่เอามาดัดแปลงประยุกต์ใช้กับสาขาลูก เช่น เมนูข้าวมันไก่ของสาขาแม่ 50 บาท แต่สาขาลูกอยากจะขายในราคา 60 บาทก็จะเกิิดการเปลี่ยนแปลงข้อมูลและนำข้อมูลที่เขียนทับมาไว้ใน branch_override

| Name | Type | Description
| ----|----|-----------  
{branchOverride_uuid} | {object} | ...

#### branchOverride_uuid
| Name | Type | Description
| ----|----|-----------  
accounting | {object} | ...
departmentGroups | {object} | ...
departments | {object} | ...
promotion | {object} | ...
topping | {object} | ...

#### accounting
| Name | Type | Description
| ----|----|-----------  
{accounting_uuid} | {object} | uuid

#### accounting_uuid
| Name | Type | Description
| ----|----|-----------  
uuid\* | string | รหัส?
computeMode | number| วิธีการคำนวน `0=คิดจากยอดsub total,1=คิดหลังจากหักลดสินค้าแล้ว,2=สะสมยอดแต่ละบรรทัด`
mode | number | `0= % , 1= Baht`
modeValue | number | จำนวนเงิน Baht หรือ %

#### departmentGroups            
| Name | Type | Description
| ----|----|-----------  
{departmentGroups_uuid} | {object} | uuid

#### departmentGroups_uuid            
| Name | Type | Description
| ----|----|-----------  
printer | {object boolean} | เลข printer ที่ active `3: true`

#### departments
| Name | Type | Description
| ----|----|-----------  
{departments_uuid} | {object} | uuid ของรายการเมนูนั้น ๆ

#### departments_uuid
| Name | Type | Description
| ----|----|-----------  
price | number | ราคา

#### promotion
| Name | Type | Description
| ----|----|-----------  
{promotion_key} | {object} | key ของ promotion นั้น ๆ

#### promotion_key
| Name | Type | Description
| ----|----|-----------
isActive | boolean | กำลังเปิดใช้โปรโมชั่นนั้น ๆ อยู่หรือไม่

#### topping
| Name | Type | Description
| ----|----|-----------  
{topping_uuid} | {object} | uuid ของ topping นั้น ๆ 

#### topping_uuid
| Name | Type | Description
| ----|----|-----------  
price | number | ราคาtopping

### departments (menu เมนูอาหาร)
| Name | Type | Description
| ----|----|-----------  
{departments_uuid} | {object} | `3180`

#### departments_uuid
| Name | Type | Description
| ----|----|-----------  
{menuGroup_uuid} | {object} | `lcAJh5kx`

#### menuGroup_uuid
| Name | Type | Description
| ----|----|-----------  
items | {object} | เมนู?
row | number | หมายเลขแถวแสดงผล
type | string | `dorKIohG`
uuid | string | `lcAJh5kx`

#### items
| Name | Type | Description
| ----|----|-----------  
{item_uuid}| {object}| uuid ของ menu items `3d9DWZEE`
name | string | ชื่อ ของ menu group `ข้าวแกง`
printer | {object} | เลข printer ที่ active `"3": true`

#### item_uuid
| Name | Type | Description
| ----|----|-----------  
name | string | ชื่อ menu items `ข้าวผัดกระเพาหมู`
price | number | ราคา menu items
row | number | หมายเลขแถวแสดงผล
subItems | {object} | uuid ของ menu sub-items `EsumME0B`     
uuid | string | uuid ของ menu items `3d9DWZEE`


#### subItem_uuid
| Name | Type | Description
| ----|----|-----------  
name | string | ชื่อ menu sub-items `พิเศษ`
price | number | ราคา menu sub-items
row | number | หมายเลขแถวแสดงผล
uuid | string | uuid ของ menu sub-items `EsumME0B`

#### printer
| Name | Type | Description
| ----|----|-----------  
{printer no.} | boolean | เลข printer ที่ active `"3": true`

### department type (ชนิดของ menu อาหาร)
| Name | Type | Description
| ----|----|-----------  
{departments_uuid2} | {object} | `3180`

#### departments_uuid2
| Name | Type | Description
| ----|----|-----------
{departmenttype_uuid} | {object} |  `SidItSST`

#### departmenttype_uuid
| Name | Type | Description
| ----|----|-----------
name| string |`Dessert`
row | number | หมายเลขแถวแสดงผล
uuid| string | `SidItSST`


### employees พนักงาน
| Name | Type | Description
| ----|----|-----------
{departments_uuid3} | {object} | `3180`

#### departments_uuid3
| Name | Type | Description
| ----|----|-----------
{employees_uuid} | {object} | `-KpxeEJBgv0oYG9fmssz`

#### employees_uuid
| Name | Type | Description
|----|----|-----------  
name | string |ชื่อพนักงาน `Win`
password | string | รหัสผ่าน
permission | number | หมายเลขสิทธิ์ `400 = manager`
remark | string | บันทึกข้อความ

### expense รายจ่าย
| Name | Type | Description
|----|----|-----------  
{departments_uuid4} | {object} | `3180`

#### departments_uuid4
| Name | Type | Description
|----|----|-----------  
name| ค่าซ่อมอุปกรณ์|ชื่อกลุ่ม expense นั้น ๆ
row | number | หมายเลขแถวแสดงผล
{expense key} | {object} | expense key `-KokDxug302BOkdHYn6k`

#### expense key
| Name | Type | Description
|----|----|-----------  
items| {object} | expense items

#### expense items
| Name | Type | Description
|----|----|-----------  
{expenseKey_uuid} | {object} | `-KovK-QrAt6pZuHgP1pr`

#### expenseKey_uuid
| Name | Type | Description
|----|----|-----------  
name| string |ชื่อกลุ่ม items นั้น ๆ `ปริ๊นเตอร์ `
row | number | หมายเลขแถวแสดงผล
    
### permissionList
| Name | Type | Description
|----|----|-----------  
{departments_uuid4} | {object} | `3180`

#### departments_uuid4
| Name | Type | Description
|----|----|-----------  
{permissionList_uuid} | {object} | `-KpxkyemXB75N0zDFTgg`

#### permissionList_uuid
| Name | Type | Description
|----|----|-----------  
name | string | `Manager`
feature | {object} | features ต่าง ๆ ที่ใช้ได้
pos | {object} | ทำอะไรกับ pos ได้บ้าง

#### feature(permissionList)
| Name | Type | Description
|----|----|-----------  
expense | boolean | true,
feature_all | boolean | true,
inventory | boolean | true,
menu | boolean | true,
pos | boolean | true,
report | boolean | true,
setting | boolean | true

#### pos(permissionList)
| Name | Type | Description
|----|----|-----------  
pos_all | boolean | true,
pos_discount | boolean | true,
pos_hideCashier | boolean | true,
pos_move | boolean | true,
pos_payment | boolean | true,
pos_void | boolean | true

### productPrintLabel AND comboSet
> product print label = ชื่อรองของเมนูนั้น ๆ ,comboset คือสั่งอารเป็นชุดเช่น สั่งข้าวมันไก่ แล้วได้ข้าวขาหมูด้วย

| Name | Type | Description
|----|----|-----------  
{departments_uuid5} | {object} | `3180`
        
#### departments_uuid5
| Name | Type | Description
|----|----|-----------  
{productPrintLabel_uuid} | {object} | uuid ของ menu นั้น ๆ `ixZuvsOp`

#### productPrintLabel_uuid
| Name | Type | Description
|----|----|-----------  
kitchenName | string | `Kaow mun kai`
secondName | string | `Kaow MKai`
comboList | {object} | ... 

#### combolist
| Name | Type | Description
|----|----|-----------  
{menu_uuid}| object | uuid ของ menu นั้น ๆ `tM8hA5NG : 1`



