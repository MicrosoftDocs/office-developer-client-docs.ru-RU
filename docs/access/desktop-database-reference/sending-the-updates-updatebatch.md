---
title: 'Отправка обновлений: UpdateBatch'
TOCTitle: 'Sending the Updates: UpdateBatch'
ms:assetid: a840b9a7-7ccd-9c31-7951-8921dadf381e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249778(v=office.15)
ms:contentKeyID: 48546898
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 432c54c16984135bb5492854e2a9e9ac1ca94336
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883367"
---
# <a name="sending-the-updates-updatebatch"></a><span data-ttu-id="8d57f-102">Отправка обновлений: UpdateBatch</span><span class="sxs-lookup"><span data-stu-id="8d57f-102">Sending the Updates: UpdateBatch</span></span>


<span data-ttu-id="8d57f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d57f-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="sending-the-updates-updatebatch-method"></a><span data-ttu-id="8d57f-104">Отправка обновлений: метод UpdateBatch</span><span class="sxs-lookup"><span data-stu-id="8d57f-104">Sending the Updates: UpdateBatch Method</span></span>

<span data-ttu-id="8d57f-105">Следующий код открывает **записей** в пакетном режиме путем установки свойства **LockType для** **adLockBatchOptimistic** и **CursorLocation** для **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="8d57f-105">The following code opens a **Recordset** in batch mode by setting the **LockType** property to **adLockBatchOptimistic** and the **CursorLocation** to **adUseClient**.</span></span> <span data-ttu-id="8d57f-106">Добавляется два новых записей и изменяет значение поля в существующей записи, сохранение исходных значений, а затем вызывает, **UpdateBatch** для отправки изменений обратно в источник данных.</span><span class="sxs-lookup"><span data-stu-id="8d57f-106">It adds two new records and changes the value of a field in an existing record, saving the original values, and then calls **UpdateBatch** to send the changes back to the data source.</span></span>

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

<span data-ttu-id="8d57f-107">При изменении текущей записи или добавления новой записи при вызове метода **UpdateBatch** , ADO автоматически будет вызвать метод **Update** для сохранения всех ожидающих изменений в текущей записи перед передачей пакетные изменения Поставщик.</span><span class="sxs-lookup"><span data-stu-id="8d57f-107">If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

