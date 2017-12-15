# Niceloop_info
> infomation in niceloop pos

`* = required`

### infoRoot
| Name | Type | Description
| ----|----|-----------  
table | string | โต๊ะลูกค้า
info | [{object}](info.md#infoobject) | ...
             
### InfoObject
| Name | Type | Description
| ----|----|-----------  
isLock | boolean |  โตีะถูกล็อกมั้ย     
guest | number| จำนวนลูกค้า          
comment | array of string |  " ['string', ...]"
member | [{object}](member.md#member)| ลูกค้าสมาชิก        
openTime | string |  เวลาเปิด??
noOfPrintPreview | number |  จำนวนสั่งปริ้นพรีวิว
addOn | [array object](receipt.md#addon) |  ส่วนเพิ่มเติม