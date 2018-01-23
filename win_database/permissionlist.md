# Niceloop_info
> infomation in niceloop pos

`* = required`

### permissionList
| Name | Type | Description
|----|----|-----------  
{departments_uuid5} | [{object}](z_part1.md#departments_uuid5) | `3180`

#### departments_uuid5
| Name | Type | Description
|----|----|-----------  
{permissionList_uuid} | [{object}](z_part1.md#permissionlist_uuid) | `-KpxkyemXB75N0zDFTgg`

#### permissionList_uuid
| Name | Type | Description
|----|----|-----------  
name | string | `Manager`
feature | [{object}](z_part1.md#featurepermissionlist) | features ต่าง ๆ ที่ใช้ได้
pos | [{object}](z_part1.md#pospermissionlist) | ทำอะไรกับ pos ได้บ้าง

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