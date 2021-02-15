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
# <a name="address-book-navigation-buttons"></a><span data-ttu-id="9ecae-102">Кнопки навигации по адресной книге</span><span class="sxs-lookup"><span data-stu-id="9ecae-102">Address Book navigation buttons</span></span>

<span data-ttu-id="9ecae-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ecae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9ecae-104">Приложение адресной книги отображает кнопки навигации в нижней части веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="9ecae-104">The Address Book application displays the navigation buttons at the bottom of the webpage.</span></span> <span data-ttu-id="9ecae-105">Вы можете использовать кнопки навигации для навигации по данным в сетке HTML, выбрав первую или последнюю строку данных или строки, расположенные рядом с текущим выделением.</span><span class="sxs-lookup"><span data-stu-id="9ecae-105">You can use the navigation buttons to navigate through the data in the HTML grid display by selecting either the first or last row of data, or rows adjacent to the current selection.</span></span>

## <a name="navigation-sub-procedures"></a><span data-ttu-id="9ecae-106">Под процедуры навигации</span><span class="sxs-lookup"><span data-stu-id="9ecae-106">Navigation Sub Procedures</span></span>

<span data-ttu-id="9ecae-107">Приложение адресной книги содержит несколько процедур, позволяющих пользователям нажимать  кнопки "Первый", "Далее", "Назад" и "Последний" для перемещения данных. </span><span class="sxs-lookup"><span data-stu-id="9ecae-107">The Address Book application contains several procedures that allow users to click the **First**, **Next**, **Previous**, and **Last** buttons to move around the data.</span></span>

<span data-ttu-id="9ecae-108">Например, нажатие кнопки **"Первый"** активирует процедуру VBScript First \_ OnClick Sub.</span><span class="sxs-lookup"><span data-stu-id="9ecae-108">For example, clicking the **First** button activates the VBScript First\_OnClick Sub procedure.</span></span> <span data-ttu-id="9ecae-109">Процедура выполняет метод [MoveFirst,](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) который делает первую строку данных текущим выделением.</span><span class="sxs-lookup"><span data-stu-id="9ecae-109">The procedure executes a [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) method, which makes the first row of data the current selection.</span></span> <span data-ttu-id="9ecae-110">Нажатие кнопки **"Последний"** активирует процедуру Last OnClick Sub, которая вызывает метод MoveLast, делая последнюю строку данных \_ текущим выделением. [](movefirst-movelast-movenext-and-moveprevious-methods-rds.md)</span><span class="sxs-lookup"><span data-stu-id="9ecae-110">Clicking the **Last** button activates the Last\_OnClick Sub procedure, which invokes the [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) method, making the last row of data the current selection.</span></span> <span data-ttu-id="9ecae-111">Остальные кнопки навигации работают аналогично.</span><span class="sxs-lookup"><span data-stu-id="9ecae-111">The remaining navigation buttons work in a similar fashion.</span></span>

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

