# expense (win_db)
> expense (win_db) in niceloop pos

`* = required`

### expense รายจ่าย
| Name | Type | Description
|----|----|-----------  
{departments_uuid4} | [{object}](z_part1.md#departments_uuid4) | `3180`

#### departments_uuid4
| Name | Type | Description
|----|----|-----------  
name| ค่าซ่อมอุปกรณ์|ชื่อกลุ่ม expense นั้น ๆ
row | number | หมายเลขแถวแสดงผล
{expense_key} | [{object}](z_part1.md#expensekey) | expense key `-KokDxug302BOkdHYn6k`

#### expense_key
| Name | Type | Description
|----|----|-----------  
items| [{object}](z_part1.md#expense_items) | expense items

#### expense_items
| Name | Type | Description
|----|----|-----------  
{expenseKey_uuid} | [{object}](z_part1.md#expensekey_uuid) | `-KovK-QrAt6pZuHgP1pr`

#### expenseKey_uuid
| Name | Type | Description
|----|----|-----------  
name| string |ชื่อกลุ่ม items นั้น ๆ `ปริ๊นเตอร์ `
row | number | หมายเลขแถวแสดงผล