### expense_transactions
>expense_transactions (รายการของรายจ่ายที่ถูกบันทึก)

| Name | Type | Description
| ----|----|-----------  
let expense_transactions = [{
    uuid: "1VCIGKGv",
    amount: 20,
    businessDate: "2017-10-18",
    comment: "",
    customerId: '3180',
    dateTime: "2017-10-17T17:00:00.000Z",
    flag: false,
    group: "ค่าซ่อมอุปกรณ์",
    groupKey: "-KokDxug302BOkdHYn6k",
    item: "ปริ๊นเตอร์",
    itemKey: "kfepofkopf2",
    uuid: 'fkeofoe'//uuid ข้อง transaction นั้น ๆ

}]

### inventoryGroup
>inventoryGroup (กลุ่มของ inventory)

| Name | Type | Description
| ----|----|-----------  
let inventoryGroup = [{
    "customerId": "3180",
    "name": "ff23",
    "row": 1,
    "uuid": "XkORRIhJ" //uuid กลุ่ม
}]

### inventory
>inventory (รายการ inventory)

| Name | Type | Description
| ----|----|-----------  
let inventory = [{
    "uuid": "mZMpRyey", //uuid invemtory    
    "balance": 101, // จำนวนคงเหลือปัจจุบัน
    "baseUnit": "can",  //หน่วยหลัก เช่น กระป๋อง
    "converter": { //เก็บค่าของหน่วยต่าง ๆ
        "Box": 100,//เช่น Pepsi 1 Box บรรจุ Pepsi 100 กระป๋อง
        "can": 1,
        "Pack": 12
    },
    "customerId": "3180",
    "groupUuid": "f2eff2f211ccc",
    "name": "Pepsi",
    "recieveUnit": "Pack", //หน่วยรับ (สำหรับหน้า เพิ่มของเข้า stock)
    "reportUnit": "Box", // หน่วยที่โชว์เวลาแสดงผล
    "row": 0,
    "safetyStock": 252, //จำนวน safety สำหรับแจ้งว่าของไกล้หมด
    "safetyStockUnit": "Pack",
    "safetyStockValue": "21",
}]

### InventoryTransaction
>InventoryTransaction (ประวัติการเพิ่มลง stock)

| Name | Type | Description
| ----|----|-----------  
let InventoryTransaction = [{
    "amount": 48, //จำนวนสินค้าเหลือเก่า + จำนวนสินค้าใหม่ เช่น สินค้าเก่ามี 24 + สินค้าใหม่เพิ่มเข้ามา 24 = 48
    "businessDay": "2017-09-16",
    "customerId": "3180",
    "dateTime": "2017-09-16T04:41:47.166Z",
    "inputAmount": 24, //จำนวน สินค้าที่เพิ่มเข้า stock
    "localTime": "2017-09-16T11:41:47+07:00",
    "type": 4,
    "uuid": "3Ms9RMUE"
}]

### formula
>formula (สูตรเมนูอาหาร)

| Name | Type | Description
| ----|----|-----------  
let formula = [{
    "customerId": "3180",
    "formula": {
        "mZMpRyey": 2 //uuid ของ inventory item
    },
    "uuid": "3rbWZixj"//uuid ของ menu item
}]

### ToppingFormula
| Name | Type | Description
| ----|----|-----------  
let ToppingFormula = [{
    "customerId": "3180",
    "formula": {
        "YnNdiQoz": 4 //uuid ของ inventory item
    },
    "uuid": "MoIfxWPu" //uuid ของ topping item
}] 