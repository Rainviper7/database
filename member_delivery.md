# Niceloop\_member\_delivery
> Member delivery in niceloop pos

`* = required`

### member_delivery
| Name | Type | Description
| ----|----|-----------
uuid\* | string | ...
customerId | string | รหัสลูกค้า
branchId | string | หมายเลขรหัสสาขา
birthDate | datetime | วันเกิด
firstName | string | ชื่อ
lastName | string | นามสกุล
gender | string | เพศ
channel | [{object}](member_delivery.md#channel) | ช่องทางติดต่อ
zone | [{object}](member_delivery.md#zone) | โซน ที่อยุ่
note | string | บันทึกข้อความ
tel | string | เบอร์โทศัพท์

### channel
| Name | Type | Description
| ----|----|-----------
uuid\*| string | `fwfe1f111`
name| string | ชื่อช่องทาง `Facebook`

### zone
| Name | Type | Description
| ----|----|-----------
uuid\*| string | `fefewfw11`
name| string | ชื่อโซน `Lardprow`
