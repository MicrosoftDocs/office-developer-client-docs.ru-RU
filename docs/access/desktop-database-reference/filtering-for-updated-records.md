---
title: Фильтрация для обновленных записей
TOCTitle: Filtering for updated records
ms:assetid: 0dc22b0a-3501-078d-788c-40aa97f2e644
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248857(v=office.15)
ms:contentKeyID: 48543229
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3bf6619b9b375642bc9f279aea92cb20df3b859
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947814"
---
# <a name="filtering-for-updated-records"></a>Фильтрация для обновленных записей

**Применимо к**: Access 2013, Office 2013

## <a name="filtering-for-updated-records"></a>Фильтрация для обновленных записей

До вызова метода **UpdateBatch**, можно использовать свойство **фильтра** **набора записей** для просмотра только тех записей, которые были изменены с момента открытия **набора записей** или последнего вызова **UpdateBatch**. Чтобы сделать это, равным **фильтра** **adFilterPendingRecords** , чтобы определить, сколько записей будут обновлены, как показано ниже.

Этот пример демонстрирует расширение в предыдущем примере **UpdateBatch** путем фильтрации **набора записей** до вызова **UpdateBatch**, отображение пользователем записи изменится и позволяя ему для отмены обновления (с помощью **CancelBatch** метод).

```vb 
 
'BeginFilterAffected 
    objRs1.Filter = adFilterPendingRecords 
    objRs1.MoveFirst 
     
    strMsg = "The following " & objRs1.RecordCount & " values will " & _ 
             "be updated. Do you wish to proceed?" 
    While Not objRs1.EOF 
        strMsg = strMsg & vbCrLf & objRs1(0) & vbTab & objRs1(1) & vbTab & _ 
                 objRs1(2) & vbCrLf 
        objRs1.MoveNext 
    Wend 
     
    blnResp = MsgBox(strMsg, vbYesNo, "Proceed with Update?") 
    If blnResp = True Then 
        objRs1.UpdateBatch 
    Else 
        objRs1.CancelBatch 
    End If 
'EndFilterAffected 
```

