---
title: 'Шаг 4: Заполните текстовое поле сведений'
TOCTitle: 'Step 4: Populate the Details Text Box'
ms:assetid: fa5e4482-8986-0c03-1e46-7b7fefb5fb58
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250278(v=office.15)
ms:contentKeyID: 48548839
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e0f04d52edc55c7ccc5163bc9a858d7bc8845702
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481614"
---
# <a name="step-4-populate-the-details-text-box"></a><span data-ttu-id="233c1-102">Шаг 4: Заполните текстовое поле сведений</span><span class="sxs-lookup"><span data-stu-id="233c1-102">Step 4: Populate the Details Text Box</span></span>


<span data-ttu-id="233c1-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="233c1-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-4-populate-the-details-text-box"></a><span data-ttu-id="233c1-104">Шаг 4: Заполните текстовое поле сведений</span><span class="sxs-lookup"><span data-stu-id="233c1-104">Step 4: Populate the Details Text Box</span></span>

<span data-ttu-id="233c1-105">**Для заполнения текстовом поле сведений**</span><span class="sxs-lookup"><span data-stu-id="233c1-105">**To populate the Details text box**</span></span>

<span data-ttu-id="233c1-106">Создание нового подпрограммы с именем recFields и вставьте следующий код:</span><span class="sxs-lookup"><span data-stu-id="233c1-106">Create a new subroutine named recFields and insert the following code:</span></span>

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

<span data-ttu-id="233c1-107">Этот код заполняет lstDetails с полями и значения простой записи, передаваемые recFields.</span><span class="sxs-lookup"><span data-stu-id="233c1-107">This code populates lstDetails with the fields and values of the simple record passed to recFields.</span></span> <span data-ttu-id="233c1-108">Если ресурс является текстовым файлом, текст **поток** открывается из записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="233c1-108">If the resource is a text file, a text **Stream** is opened from the resource record.</span></span> <span data-ttu-id="233c1-109">Код определяет, если набор знаков ASCII и копирует содержимое **потока** в txtDetails.</span><span class="sxs-lookup"><span data-stu-id="233c1-109">The code determines if the character set is ASCII and copies the **Stream** contents into txtDetails.</span></span>

