---
title: 'Шаг 3: Заполнения списка полей'
TOCTitle: 'Step 3: Populate the Fields List Box'
ms:assetid: b304d3a1-2237-d6f5-6e32-c6e5b9946e10
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249855(v=office.15)
ms:contentKeyID: 48547187
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ca764e2339d0c866922be2982a168afc03d84c1d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480430"
---
# <a name="step-3-populate-the-fields-list-box"></a><span data-ttu-id="7f4d1-102">Шаг 3: Заполнения списка полей</span><span class="sxs-lookup"><span data-stu-id="7f4d1-102">Step 3: Populate the Fields List Box</span></span>


<span data-ttu-id="7f4d1-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f4d1-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-3-populate-the-fields-list-box"></a><span data-ttu-id="7f4d1-104">Шаг 3: Заполнения списка полей</span><span class="sxs-lookup"><span data-stu-id="7f4d1-104">Step 3: Populate the Fields List Box</span></span>

<span data-ttu-id="7f4d1-105">**Для заполнения списка полей**</span><span class="sxs-lookup"><span data-stu-id="7f4d1-105">**To populate the Fields list box**</span></span>

<span data-ttu-id="7f4d1-106">Вставьте следующий код в обработчик событий Click lstMain:</span><span class="sxs-lookup"><span data-stu-id="7f4d1-106">Insert the following code into the Click event handler of lstMain:</span></span>

```vb 
 
Private Sub lstMain_Click() 
    Dim rec As Record 
    Dim rs As Recordset 
    Set rec = New Record 
    Set rs = New Recordset 
    grs.MoveFirst 
    grs.Move lstMain.ListIndex 
    lstDetails.Clear 
    rec.Open grs 
    Select Case rec.RecordType 
        Case adCollectionRecord: 
            Set rs = rec.GetChildren 
            While Not rs.EOF 
                lstDetails.AddItem rs(0) 
                rs.MoveNext 
            Wend 
        Case adSimpleRecord: 
            recFields rec, lstDetails, txtDetails 
             
        Case adStructDoc: 
    End Select 
     
End Sub 
```

<span data-ttu-id="7f4d1-107">Этот код объявляет и создает экземпляр локальной **записи** и объектов **наборов записей** , записи и и rs, соответственно.</span><span class="sxs-lookup"><span data-stu-id="7f4d1-107">This code declares and instantiates local **Record** and **Recordset** objects, rec and and rs, respectively.</span></span>

<span data-ttu-id="7f4d1-108">Строка, соответствующий ресурсов, выбранных в lstMain становится текущей строки grs.</span><span class="sxs-lookup"><span data-stu-id="7f4d1-108">The row corresponding to the resource selected in lstMain is made the current row of grs.</span></span> <span data-ttu-id="7f4d1-109">Затем **сведения о** списке флажка и открывается записей с текущей строки.</span><span class="sxs-lookup"><span data-stu-id="7f4d1-109">Then the **Details** list box is cleared and rec is opened with the current row of .</span></span> <span data-ttu-id="7f4d1-110">Затем **сведения о** списке флажка и открывается с текущей строки grs в качестве источника записей.</span><span class="sxs-lookup"><span data-stu-id="7f4d1-110">Then the **Details** list box is cleared and rec is opened with the current row of grs as the source.</span></span>

<span data-ttu-id="7f4d1-111">Если ресурс является записью семейства сайтов (в соответствии с **типом записи**), локального **набора записей**, rs, открывается на дочерних записей. Затем lstDetails заполняется значениями из строки открывается на дочерних записей. Затем lstDetails заполняется значениями из строки rs.</span><span class="sxs-lookup"><span data-stu-id="7f4d1-111">If the resource is a collection record (as specified by **RecordType**), the local **Recordset**, rs, is opened on the children of rec. Then lstDetails is filled with the values from the rows of is opened on the children of rec. Then lstDetails is filled with the values from the rows of rs.</span></span>

<span data-ttu-id="7f4d1-112">Если простой записи ресурса, называется recFields.</span><span class="sxs-lookup"><span data-stu-id="7f4d1-112">If the resource is a simple record, recFields is called.</span></span> <span data-ttu-id="7f4d1-113">Дополнительные сведения о recFields можно следующим шагом.</span><span class="sxs-lookup"><span data-stu-id="7f4d1-113">For more information about recFields, see the next step.</span></span>

<span data-ttu-id="7f4d1-114">Код не реализуется, если ресурса структурированных документов.</span><span class="sxs-lookup"><span data-stu-id="7f4d1-114">No code is implemented if the resource is a structured document.</span></span>

