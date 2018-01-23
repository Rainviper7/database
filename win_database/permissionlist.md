# Niceloop_permissionlist
> infomation in niceloop pos

`* = required`

#### permissionList_uuid
| Name | Type | Description
|----|----|-----------  
name | string | `Manager`
feature | [{feature}](permissionlist.md#feature) | features ต่าง ๆ ที่ใช้ได้
pos | [{pos}](permissionlist.md#pos) | ทำอะไรกับ pos ได้บ้าง

#### feature
| Name | Type | Description
|----|----|-----------  
expense | boolean | true
feature_all | boolean | true
inventory | boolean | true
menu | boolean | true
pos | boolean | true
report | boolean | true
setting | boolean | true

#### pos
| Name | Type | Description
|----|----|-----------  
pos_all | boolean | true
pos_discount | boolean | true
pos_hideCashier | boolean | true
pos_move | boolean | true
pos_payment | boolean | true
pos_void | boolean | true