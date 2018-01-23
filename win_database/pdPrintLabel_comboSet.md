# productPrintLabel AND comboSet (win_db)
> product print label = ชื่อรองของเมนูนั้น ๆ ,comboset คือสั่งอารเป็นชุดเช่น สั่งข้าวมันไก่ แล้วได้ข้าวขาหมูด้วย

`* = required`

| Name | Type | Description
|----|----|-----------  
{departments_uuid6} | [{object}](z_part1.md#departments_uuid6) | `3180`
        
#### departments_uuid6
| Name | Type | Description
|----|----|-----------  
{productPrintLabel_uuid} | [{object}](z_part1.md#productprintlabel_uuid) | uuid ของ menu นั้น ๆ `ixZuvsOp`

#### productPrintLabel_uuid
| Name | Type | Description
|----|----|-----------  
kitchenName | string | `Kaow mun kai`
secondName | string | `Kaow MKai`
comboList | [{object}](z_part1.md#combolist) | ... 

#### combolist
| Name | Type | Description
|----|----|-----------  
{menu_uuid}| object | uuid ของ menu นั้น ๆ `tM8hA5NG : 1`