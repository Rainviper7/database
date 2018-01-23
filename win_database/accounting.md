# accounting (win_db)
> infomation in niceloop pos

`* = required`

| Name | Type | Description
|----|----|-----------  
uuid\* | string | รหัส?
accountType | number | ชนิดของ account `0=assets,1=liability,2=equity,3=revennu 4=expence`
computeMode | number| วิธีการคำนวน `0=คิดจากยอดsub total,1=คิดหลังจากหักลดสินค้าแล้ว,2=สะสมยอดแต่ละบรรทัด`
mode | number | `0= % , 1= Baht`
modeValue | number | จำนวนเงิน Baht หรือ %
name | stirng | Discount Voucher
row | number | หมายเลขแถวแสดงผล