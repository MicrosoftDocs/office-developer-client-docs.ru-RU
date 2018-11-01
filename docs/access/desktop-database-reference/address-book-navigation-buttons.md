---
title: Кнопки навигации по адресной книге
TOCTitle: Address Book Navigation Buttons
ms:assetid: 4ec32c08-5b35-8dce-23ec-0daa4db551cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249253(v=office.15)
ms:contentKeyID: 48544765
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d0a6409bcdeca211c3badb1ca7918d3d34bc3f1f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869024"
---
# <a name="address-book-navigation-buttons"></a><span data-ttu-id="2d703-102">Кнопки навигации по адресной книге</span><span class="sxs-lookup"><span data-stu-id="2d703-102">Address Book Navigation Buttons</span></span>


<span data-ttu-id="2d703-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d703-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2d703-104">Адресная книга приложения отображаются кнопки навигации в нижней части веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="2d703-104">The Address Book application displays the navigation buttons at the bottom of the webpage.</span></span> <span data-ttu-id="2d703-105">Можно использовать кнопки перехода для перемещения по данным в отображение сетки HTML, выбрав либо первой или последней строки данных или рядом с текущего выделения строк.</span><span class="sxs-lookup"><span data-stu-id="2d703-105">You can use the navigation buttons to navigate through the data in the HTML grid display by selecting either the first or last row of data, or rows adjacent to the current selection.</span></span>

## <a name="navigation-sub-procedures"></a><span data-ttu-id="2d703-106">Процедуры Sub навигации</span><span class="sxs-lookup"><span data-stu-id="2d703-106">Navigation Sub Procedures</span></span>

<span data-ttu-id="2d703-107">Приложение адресная книга содержит некоторые процедуры, которые позволяют пользователям щелкните **первый**, **Далее**, **Назад**и **последний** кнопки для перемещения данных.</span><span class="sxs-lookup"><span data-stu-id="2d703-107">The Address Book application contains several procedures that allow users to click the **First**, **Next**, **Previous**, and **Last** buttons to move around the data.</span></span>

<span data-ttu-id="2d703-108">Например, щелкнув **Первая** кнопка активирует первый VBScript\_процедуры OnClick Sub.</span><span class="sxs-lookup"><span data-stu-id="2d703-108">For example, clicking the **First** button activates the VBScript First\_OnClick Sub procedure.</span></span> <span data-ttu-id="2d703-109">Процедура выполняет метод [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) , что делает первую строку данных текущего выделенного фрагмента.</span><span class="sxs-lookup"><span data-stu-id="2d703-109">The procedure executes a [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) method, which makes the first row of data the current selection.</span></span> <span data-ttu-id="2d703-110">Нажатие кнопки **последней** активирует последний\_процедуры OnClick Sub, которая вызывает метод [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) текущего выделения последней строки данных.</span><span class="sxs-lookup"><span data-stu-id="2d703-110">Clicking the **Last** button activates the Last\_OnClick Sub procedure, which invokes the [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) method, making the last row of data the current selection.</span></span> <span data-ttu-id="2d703-111">Аналогичным образом работать оставшихся кнопок навигации.</span><span class="sxs-lookup"><span data-stu-id="2d703-111">The remaining navigation buttons work in a similar fashion.</span></span>

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

