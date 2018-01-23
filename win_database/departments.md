# departments (win_db)
> departments (win_db) in niceloop pos

`* = required`

| Name | Type | Description
| ----|----|-----------  
items | [{items}](departments.md#items) | เมนู?
row | number | หมายเลขแถวแสดงผล
type | string | `dorKIohG`
uuid | string | `lcAJh5kx`

#### items
| Name | Type | Description
| ----|----|-----------  
{item_uuid}| [{item_uuid}](departments.md#item_uuid) | uuid ของ menu items `3d9DWZEE`
name | string | ชื่อ ของ menu group `ข้าวแกง`
printer | object | เลข printer ที่ active `{"1": false,"3": true}`

#### item_uuid
| Name | Type | Description
| ----|----|-----------  
name | string | ชื่อ menu items `ข้าวผัดกระเพาหมู`
price | number | ราคา menu items
row | number | หมายเลขแถวแสดงผล
subItems | [{object}](departments.md#subitem_uuid) | uuid ของ menu sub-items `EsumME0B`     
uuid | string | uuid ของ menu items `3d9DWZEE`

#### subItem_uuid
| Name | Type | Description
| ----|----|-----------  
name | string | ชื่อ menu sub-items `พิเศษ`
price | number | ราคา menu sub-items
row | number | หมายเลขแถวแสดงผล
uuid | string | uuid ของ menu sub-items `EsumME0B`