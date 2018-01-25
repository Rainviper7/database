# inventory
>inventory (รายการ inventory)

| Name | Type | Description
| ----|----|-----------  
uuid | string |  uuid invemtory  `mZMpRyey` 
balance | number | จำนวนคงเหลือปัจจุบัน `101`  
baseUnit | string | หน่วยหลัก เช่น กระป๋อง `can`  
converter | [{converter}](inventory.md#converter) |   เก็บค่าของหน่วยต่าง ๆ
customerId | string |   `3180`
groupUuid | string |   `f2eff2f211ccc`
name | string | `Pepsi`
recieveUnit | string | หน่วยรับ (สำหรับหน้า เพิ่มของเข้า stock)  `Pack` 
reportUnit | string | หน่วยที่โชว์เวลาแสดงผล  `Box`
row | number | หมายเลขแถวแสดงผล
safetyStock | number | จำนวน safety สำหรับแจ้งว่าของไกล้หมด `252`
safetyStockUnit | string |   `Pack`
safetyStockValue | string |   `"21"`

#### converter
| Name | Type | Description
| ----|----|-----------  
Box | number |  เช่น Pepsi 1 Box บรรจุ Pepsi 100 กระป๋อง `100`
can | number |   `1`
Pack | number |   `12`