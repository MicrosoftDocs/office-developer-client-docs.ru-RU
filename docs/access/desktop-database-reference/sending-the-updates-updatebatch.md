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
# <a name="sending-the-updates-updatebatch"></a><span data-ttu-id="f54c3-102">Отправка обновлений: UpdateBatch</span><span class="sxs-lookup"><span data-stu-id="f54c3-102">Sending the updates: UpdateBatch</span></span>


<span data-ttu-id="f54c3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f54c3-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="sending-the-updates-updatebatch-method"></a><span data-ttu-id="f54c3-104">Отправка обновлений: метод UpdateBatch</span><span class="sxs-lookup"><span data-stu-id="f54c3-104">Sending the Updates: UpdateBatch Method</span></span>

<span data-ttu-id="f54c3-105">Следующий код открывает объект **Recordset** в пакетном режиме, устанавливая для свойства **LockType** значение **адлоккбатчоптимистик** , а для **CursorLocation** — **адусеклиент**.</span><span class="sxs-lookup"><span data-stu-id="f54c3-105">The following code opens a **Recordset** in batch mode by setting the **LockType** property to **adLockBatchOptimistic** and the **CursorLocation** to **adUseClient**.</span></span> <span data-ttu-id="f54c3-106">Он добавляет две новые записи и изменяет значение поля в существующей записи, сохраняет исходные значения, а затем вызывает **UpdateBatch** для отправки изменений обратно в источник данных.</span><span class="sxs-lookup"><span data-stu-id="f54c3-106">It adds two new records and changes the value of a field in an existing record, saving the original values, and then calls **UpdateBatch** to send the changes back to the data source.</span></span>

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

<span data-ttu-id="f54c3-107">Если вы редактируете текущую запись или добавляете новую запись при вызове метода **UpdateBatch** , ADO автоматически вызывает метод **Update** для сохранения всех ожидающих изменений в текущей записи, прежде чем передавать пакетные изменения в поставщики.</span><span class="sxs-lookup"><span data-stu-id="f54c3-107">If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

