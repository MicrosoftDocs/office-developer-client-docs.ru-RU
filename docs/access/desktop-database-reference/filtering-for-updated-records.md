---
title: Поиск обновленных записей с помощью фильтра
TOCTitle: Filtering for updated records
ms:assetid: 0dc22b0a-3501-078d-788c-40aa97f2e644
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248857(v=office.15)
ms:contentKeyID: 48543229
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 791cbbd16eef7baf95fd51ab8624a04dc687166b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292400"
---
# <a name="filtering-for-updated-records"></a><span data-ttu-id="4147f-102">Поиск обновленных записей с помощью фильтра</span><span class="sxs-lookup"><span data-stu-id="4147f-102">Filtering for updated records</span></span>

<span data-ttu-id="4147f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4147f-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="filtering-for-updated-records"></a><span data-ttu-id="4147f-104">Filtering for Updated Records</span><span class="sxs-lookup"><span data-stu-id="4147f-104">Filtering for Updated Records</span></span>

<span data-ttu-id="4147f-105">Перед вызовом **UpdateBatch**можно использовать свойство **Filter** в **наборе записей** для просмотра только тех записей, которые были изменены с момента открытия **набора записей** или последнего вызова **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="4147f-105">Before you call **UpdateBatch**, you can use the **Recordset** **Filter** property to view only those records which have been changed since the **Recordset** was opened or the last call to **UpdateBatch**.</span></span> <span data-ttu-id="4147f-106">Для этого установите **Фильтр** равное **адфилтерпендингрекордс** , чтобы определить количество записей, которые будут обновлены, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="4147f-106">To do this, set **Filter** equal to **adFilterPendingRecords** to determine how many records will be updated, as shown below.</span></span>

<span data-ttu-id="4147f-107">В этом примере показано, как расширить предыдущий пример **UpdateBatch** , выполнив фильтрацию **набора записей** непосредственно перед вызовом **UpdateBatch**, отображая пользователя, какие записи будут изменены, и позволяя ему отменить обновление (с помощью **CancelBatch** метод).</span><span class="sxs-lookup"><span data-stu-id="4147f-107">This example extends the previous **UpdateBatch** example by filtering the **Recordset** just before calling the **UpdateBatch**, showing the user which records will change and allowing her to cancel the update (using the **CancelBatch** method).</span></span>

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

