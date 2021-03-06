---
title: 'Отправка обновлений: UpdateBatch'
TOCTitle: 'Sending the updates: UpdateBatch'
ms:assetid: a840b9a7-7ccd-9c31-7951-8921dadf381e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249778(v=office.15)
ms:contentKeyID: 48546898
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ca97f3ec2cbddfae4d62a72e5e6148a57abb4325
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308717"
---
# <a name="sending-the-updates-updatebatch"></a>Отправка обновлений: UpdateBatch


**Область применения**: Access 2013, Office 2013

## <a name="sending-the-updates-updatebatch-method"></a>Отправка обновлений: Метод UpdateBatch

Следующий код открывает  набор записей в пакетном режиме, задав свойство **LockType** **adLockBatchOptimistic** и **CursorLocation** **adUseClient.** Он добавляет две новые записи и изменяет значение поля в существующей записи, экономя исходные значения, а затем вызывает **UpdateBatch,** чтобы отправить изменения обратно в источник данных.

```vb 
 
'BeginBatchUpdate 
    strSQL = "SELECT ShipperId, CompanyName, Phone FROM Shippers" 
                  
    objRs1.CursorLocation = adUseClient 
    objRs1.Open strSQL, strConn, adOpenStatic, adLockBatchOptimistic, adCmdText 
     
    ' Change value of Phone field for first record in Recordset, saving value 
    ' for later restoration. 
    intId = objRs1("ShipperId") 
    strPhone = objRs1("Phone") 
     
    objRs1("Phone") = "(111) 555-1111" 
     
    'Add two new records 
    For i = 0 To 1 
        objRs1.AddNew 
        objRs1(1) = "New Shipper #" & CStr((i + 1)) 
        objRs1(2) = "(nnn) 555-" & i & i & i & i 
    Next i 
     
    ' Send the updates 
    objRs1.UpdateBatch 
'EndBatchUpdate 
```

При редактировании текущей записи или добавлении новой записи при вызове метода **UpdateBatch** ADO будет автоматически вызывать метод Update, чтобы сохранить все ожидающие изменения текущей записи перед передачей пакетных изменений поставщику. 

