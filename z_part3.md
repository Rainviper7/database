### expense_transactions [{object}]
>expense_transactions (รายการของรายจ่ายที่ถูกบันทึก)


| Name | Type | Description
| ----|----|-----------  
uuid | string | `1VCIGKGv`
amount | number | `20`
businessDate | string |   `2017-10-18`
comment | string | บันทึกข้อความ
customerId | string |   `3180`
dateTime | string |   `2017-10-17T17:00:00.000Z`
flag | boolean |   `false`
group | string |   ค่าซ่อมอุปกรณ์
groupKey | string |   `-KokDxug302BOkdHYn6k`
item | string |   `ปริ๊นเตอร์`
itemKey | string |   `kfepofkopf2`
uuid | string |  uuid ข้อง transaction นั้น ๆ  `fkeofoe`

### inventoryGroup
>inventoryGroup (กลุ่มของ inventory)

| Name | Type | Description
| ----|----|-----------  
customerId | string |   `3180`
name | string |   `ff23`
row | number | หมายเลขแถวแสดงผล
uuid | string |  uuid กลุ่ม `XkORRIhJ`


### inventory [{object}]
>inventory (รายการ inventory)

| Name | Type | Description
| ----|----|-----------  
uuid | string |  uuid invemtory  `mZMpRyey` 
balance | number | จำนวนคงเหลือปัจจุบัน `101`  
baseUnit | string | หน่วยหลัก เช่น กระป๋อง `can`  
converter | {object} |   เก็บค่าของหน่วยต่าง ๆ
customerId | string |   `3180`
groupUuid | string |   `f2eff2f211ccc`
name | string | `Pepsi`
recieveUnit | string | หน่วยรับ (สำหรับหน้า เพิ่มของเข้า stock)  `Pack` 
reportUnit | string | หน่วยที่โชว์เวลาแสดงผล  `Box`
row | number | หมายเลขแถวแสดงผล
safetyStock | number | จำนวน safety สำหรับแจ้งว่าของไกล้หมด `252`
safetyStockUnit | string |   `Pack`
safetyStockValue | string |   `"21"`

#### converter(inventory)
| Name | Type | Description
| ----|----|-----------  
Box | number |  เช่น Pepsi 1 Box บรรจุ Pepsi 100 กระป๋อง `100`
can | number |   `1`
Pack | number |   `12`

### InventoryTransaction[{object}]
>InventoryTransaction (ประวัติการเพิ่มลง stock)

| Name | Type | Description
| ----|----|-----------  
amount | number | จำนวนสินค้าเหลือเก่า + จำนวนสินค้าใหม่ เช่น สินค้าเก่ามี 24 + สินค้าใหม่เพิ่มเข้ามา 24 = 48 
businessDay | string |   `2017-09-16`
customerId | string |   `3180`
dateTime | string |   `2017-09-16T04:41:47.166Z`
inputAmount | number |จำนวน สินค้าที่เพิ่มเข้า stock    `24`
localTime | string |   `2017-09-16T11:41:47+07:00`
type | number |   4
uuid | string | `3Ms9RMUE`

### formula[{object}]
>formula (สูตรเมนูอาหาร)

| Name | Type | Description
| ----|----|-----------  
customerId | string |   `3180`
formula | object | uuid ของ inventory item `mZMpRyey : 2`
uuid | string | uuid ของ menu item `3rbWZixj`

### ToppingFormula[{object}]
| Name | Type | Description
| ----|----|----------- 
customerId | string |   `3180`
formula | object | uuid ของ inventory item `YnNdiQoz : 4` 
uuid | string |   uuid ของ topping item `MoIfxWPu`