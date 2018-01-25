# Niceloop\_setting
> Setting in niceloop pos

`* = required`

### DrawerLogs
| Name | Type | Description
| ----|----|----------- 
customerId | string | รหัสลูกค้า
businessDay | string | วัน???  
start | number |  เงินที่ใส่ในลิ้นชัก
pos | number |  ยอดขายจากระบบ  cash only
posEnding | number |  เงิน A
actualEnding | number |  เงิน B
diff | number |    'ส่วนต่างเงินในลิ้นชัก  A-B      ถ้าบวก เงินในระบบ เยอะกว่านับจริง  (เงินในลิ้นชักหาย)   ถ้าลบ   เงินในลิ้นชักเยอะกว่าที่คำนวนได้ในระบบ ( เงินได้รับเกิน)'
withdraw | [{withdraw}](setting.md#withdraw) |  '...'

### withdraw
| Name | Type | Description
| ----|----|----------- 
type | string |  'add \| withdraw'               
timestamp | string | เวลาลงบันทึก 
amount | number | ค่าเงิน 1500, -1500 ใส่เลข ลบถ้าหักออก
remark | string |  คอมเม้นต์