# Niceloop\_setting\_delivery
> Setting\_delivery in niceloop pos

`* = required`

### setting_delivery
| Name | Type | Description
| ----|----|-----------
branch | [{array object}](setting_delivery.md#branch) | สาขา 
channel | [{array object}](setting_delivery.md#chanel) |  ช่องทาง
delivery\_method | [{array object}](setting_delivery.md#delivery_method) | วิธีการจัดส่ง
zone | [{array object}](setting_delivery.md#zone) |  พื้นที่

### branch
| Name | Type | Description
| ----|----|-----------
uuid\* | string | `KiyCUaaA`
name | string | ชื่อสาขา
lat | string | ลัตติจูด
long | string | ลองจิจูด
row | string | เลขแถว
                                              
### channel 
| Name | Type | Description
| ----|----|-----------
uuid\* | string | `9qoemLBa`
name | string | ชื่อช่องทาง เช่น `Twitter` 
row | string | 1
                                               
### delivery_method
| Name | Type | Description
| ----|----|-----------
uuid\* | string | `flwf2f111`
name | string | รูปแบบการจัดส่ง `วินมอไซ`
row | string | 0
                                           
### zone
| Name | Type | Description
| ----|----|-----------
uuid\* | string | `ff22ffa`
name | string | กรุงเทพฯ
row | string | 1                                          