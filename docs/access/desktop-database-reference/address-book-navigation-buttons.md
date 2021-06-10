---
title: Кнопки навигации по адресной книге
TOCTitle: Address Book navigation buttons
ms:assetid: 4ec32c08-5b35-8dce-23ec-0daa4db551cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249253(v=office.15)
ms:contentKeyID: 48544765
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e7c87acd433df4a303c1e6a15a60184cadf994c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282466"
---
# <a name="address-book-navigation-buttons"></a><span data-ttu-id="4b5d1-102">Кнопки навигации по адресной книге</span><span class="sxs-lookup"><span data-stu-id="4b5d1-102">Address Book navigation buttons</span></span>

<span data-ttu-id="4b5d1-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b5d1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4b5d1-104">Приложение Адресная книга отображает кнопки навигации в нижней части веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="4b5d1-104">The Address Book application displays the navigation buttons at the bottom of the webpage.</span></span> <span data-ttu-id="4b5d1-105">С помощью кнопок навигации можно перемещаться по данным на дисплее HTML-сетки, выбрав первый или последний ряд данных или строки, примыкающие к текущему выбору.</span><span class="sxs-lookup"><span data-stu-id="4b5d1-105">You can use the navigation buttons to navigate through the data in the HTML grid display by selecting either the first or last row of data, or rows adjacent to the current selection.</span></span>

## <a name="navigation-sub-procedures"></a><span data-ttu-id="4b5d1-106">Навигационные под процедуры</span><span class="sxs-lookup"><span data-stu-id="4b5d1-106">Navigation Sub Procedures</span></span>

<span data-ttu-id="4b5d1-107">Приложение Адресная книга содержит несколько процедур, которые позволяют пользователям щелкнуть кнопки **First,** **Next,** **Previous** и **Last** для перемещения данных.</span><span class="sxs-lookup"><span data-stu-id="4b5d1-107">The Address Book application contains several procedures that allow users to click the **First**, **Next**, **Previous**, and **Last** buttons to move around the data.</span></span>

<span data-ttu-id="4b5d1-108">Например, щелкнув первую **кнопку,** активирует процедуру VBScript First \_ OnClick Sub.</span><span class="sxs-lookup"><span data-stu-id="4b5d1-108">For example, clicking the **First** button activates the VBScript First\_OnClick Sub procedure.</span></span> <span data-ttu-id="4b5d1-109">Процедура выполняет метод [MoveFirst,](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) который делает первый ряд данных текущим выбором.</span><span class="sxs-lookup"><span data-stu-id="4b5d1-109">The procedure executes a [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) method, which makes the first row of data the current selection.</span></span> <span data-ttu-id="4b5d1-110">Нажав  последнюю кнопку, активирует процедуру Last OnClick Sub, которая вызывает метод MoveLast, делая последний ряд данных \_ текущим выбором. [](movefirst-movelast-movenext-and-moveprevious-methods-rds.md)</span><span class="sxs-lookup"><span data-stu-id="4b5d1-110">Clicking the **Last** button activates the Last\_OnClick Sub procedure, which invokes the [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) method, making the last row of data the current selection.</span></span> <span data-ttu-id="4b5d1-111">Остальные кнопки навигации работают аналогичным образом.</span><span class="sxs-lookup"><span data-stu-id="4b5d1-111">The remaining navigation buttons work in a similar fashion.</span></span>

```vb 
 
' Move to the first record in the bound Recordset. 
Sub First_OnClick 
 DC1.Recordset.MoveFirst 
End Sub 
 
' Move to the next record from the current position 
' in the bound Recordset. 
Sub Next_OnClick 
 If Not DC1.Recordset.EOF Then ' Cannot move beyond bottom record. 
 DC1.Recordset.MoveNext 
 Exit Sub 
 End If 
End Sub 
 
' Move to the previous record from the current position in the bound 
' Recordset. 
Sub Prev_OnClick 
 If Not DC1.Recordset.BOF Then ' Cannot move beyond top record. 
 DC1.Recordset.MovePrevious 
 Exit Sub 
 End If 
End Sub 
 
' Move to the last record in the bound Recordset. 
Sub Last_OnClick 
 DC1.Recordset.MoveLast 
End Sub 
```

