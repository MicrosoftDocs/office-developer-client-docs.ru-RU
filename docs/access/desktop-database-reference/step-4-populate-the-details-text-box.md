---
title: Этап 4. Заполнение текстового поля сведений
TOCTitle: 'Step 4: Populate the Details Text Box'
ms:assetid: fa5e4482-8986-0c03-1e46-7b7fefb5fb58
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250278(v=office.15)
ms:contentKeyID: 48548839
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0c00fd9d1a13a68361c5b1a7c3c2aa39736b3c88
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867260"
---
# <a name="step-4-populate-the-details-text-box"></a><span data-ttu-id="35067-102">Этап 4. Заполнение текстового поля сведений</span><span class="sxs-lookup"><span data-stu-id="35067-102">Step 4: Populate the Details Text Box</span></span>


<span data-ttu-id="35067-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="35067-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="step-4-populate-the-details-text-box"></a><span data-ttu-id="35067-104">Этап 4. Заполнение текстового поля сведений</span><span class="sxs-lookup"><span data-stu-id="35067-104">Step 4: Populate the Details Text Box</span></span>

<span data-ttu-id="35067-105">**Для заполнения текстовом поле сведений**</span><span class="sxs-lookup"><span data-stu-id="35067-105">**To populate the Details text box**</span></span>

<span data-ttu-id="35067-106">Создание нового подпрограммы с именем recFields и вставьте следующий код:</span><span class="sxs-lookup"><span data-stu-id="35067-106">Create a new subroutine named recFields and insert the following code:</span></span>

```vb 
 
Sub recFields(r As Record, l As ListBox, t As TextBox) 
    Dim f As Field 
    Dim s As Stream 
    Set s = New Stream 
    Dim str As String 
     
    For Each f In r.Fields 
        l.AddItem f.Name & ": " & f.Value 
    Next 
    t.Text = "" 
    If r!RESOURCE_CONTENTCLASS = "text/plain" Then 
        s.Open r, adModeRead, adOpenStreamFromRecord 
        str = s.ReadText(1) 
        s.Position = 0 
        If Asc(Mid(str, 1, 1)) = 63 Then '//63 = "?" 
            s.Charset = "ascii" 
            s.Type = adTypeText 
        End If 
        t.Text = s.ReadText(adReadAll) 
    End If 
End Sub 
```

<span data-ttu-id="35067-107">Этот код заполняет lstDetails с полями и значения простой записи, передаваемые recFields.</span><span class="sxs-lookup"><span data-stu-id="35067-107">This code populates lstDetails with the fields and values of the simple record passed to recFields.</span></span> <span data-ttu-id="35067-108">Если ресурс является текстовым файлом, текст **поток** открывается из записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="35067-108">If the resource is a text file, a text **Stream** is opened from the resource record.</span></span> <span data-ttu-id="35067-109">Код определяет, если набор знаков ASCII и копирует содержимое **потока** в txtDetails.</span><span class="sxs-lookup"><span data-stu-id="35067-109">The code determines if the character set is ASCII and copies the **Stream** contents into txtDetails.</span></span>

