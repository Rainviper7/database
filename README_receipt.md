
 #Niceloop_receipt
 ##receipt bill in niceloop pos
    
 ###receipt
|----|----|-----------|
|Name|Type|Description|
|----|----|-----------|
|id|string|firestore auto gen id|
|---|---|---|

        customerId  :
          description: accountที่ใช้งาน
          type: string
          example: niceloop.pos@niceloop.com
        posId  :  
          description: เครื่องposที่ใช้งาน
          type: string
          example: 1
        hqId :  
          description: id ของ accountสาขาแม่
          type: string
          example: 123456
        datetime:
          $ref: '#/components/schemas/datetime'
        shift:
          $ref: '#/components/schemas/shift'
        user : 
          description: ชื่อพนักงานที่ใช้งานอยู่
          type: string
          example: วิภาพร
        note:
          description: บันทึกเพิ่มเติม
          type: string
          example: ชำระด้วยบัตรเครดิต
        billId :
          description: เลขที่บิล
          type: string
          example: '#00001'
        isDeleted :
          description: สถานะการลบรายการ
          type: boolean
          example: false
        deleteRemark :
          description: สถานะการลบบันทึกเพิ่มเติม
          type: boolean
          example: false
        table :
          description: หมายเลขโต๊ะ
          type: string
          example: 2