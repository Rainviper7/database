# departments (win_db)
> departments (win_db) in niceloop pos

`* = required`


| Name | Type | Description
| ----|----|-----------  
{departments_uuid} | [{object}](z_part1.md#departments_uuid) | `3180`

#### departments_uuid
| Name | Type | Description
| ----|----|-----------  
{menuGroup_uuid} | [{object}](z_part1.md#menugroup_uuid) | `lcAJh5kx`

#### menuGroup_uuid
| Name | Type | Description
| ----|----|-----------  
items | [{object}](z_part1.md#itemsmenugroup) | เมนู?
row | number | หมายเลขแถวแสดงผล
type | string | `dorKIohG`
uuid | string | `lcAJh5kx`

#### items(menuGroup)
| Name | Type | Description
| ----|----|-----------  
{item_uuid}| [{object}](z_part1.md#item_uuid)| uuid ของ menu items `3d9DWZEE`
name | string | ชื่อ ของ menu group `ข้าวแกง`
printer | [{object}](z_part1.md#printer) | เลข printer ที่ active `"3": true`

#### item_uuid
| Name | Type | Description
| ----|----|-----------  
name | string | ชื่อ menu items `ข้าวผัดกระเพาหมู`
price | number | ราคา menu items
row | number | หมายเลขแถวแสดงผล
subItems | [{object}](z_part1.md#subitem_uuid) | uuid ของ menu sub-items `EsumME0B`     
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