---
title: Address Book Navigation Buttons
TOCTitle: Address Book Navigation Buttons
ms:assetid: 4ec32c08-5b35-8dce-23ec-0daa4db551cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249253(v=office.15)
ms:contentKeyID: 48544765
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9f37a188fd3ddb3608eda414fbdcea6402cd9d41
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603947"
---
# <a name="address-book-navigation-buttons"></a><span data-ttu-id="3c4e2-102">Address Book Navigation Buttons</span><span class="sxs-lookup"><span data-stu-id="3c4e2-102">Address Book Navigation Buttons</span></span>


<span data-ttu-id="3c4e2-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c4e2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3c4e2-104"><<<<<<< HEAD. Адресная книга приложения отображаются кнопки навигации в нижней части веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="3c4e2-104"><<<<<<< HEAD The Address Book application displays the navigation buttons at the bottom of the Web page.</span></span> <span data-ttu-id="3c4e2-105">Можно использовать кнопки перехода для перемещения по данным в отображение сетки HTML, выбрав либо первой или последней строки данных или рядом с текущего выделения строк.</span><span class="sxs-lookup"><span data-stu-id="3c4e2-105">You can use the navigation buttons to navigate through the data in the HTML grid display by selecting either the first or last row of data, or rows adjacent to the current selection.</span></span>
<span data-ttu-id="3c4e2-106">=== Приложение адресной книги отображаются кнопки навигации в нижней части веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="3c4e2-106">======= The Address Book application displays the navigation buttons at the bottom of the webpage.</span></span> <span data-ttu-id="3c4e2-107">Можно использовать кнопки перехода для перемещения по данным в отображение сетки HTML, выбрав либо первой или последней строки данных или рядом с текущего выделения строк.</span><span class="sxs-lookup"><span data-stu-id="3c4e2-107">You can use the navigation buttons to navigate through the data in the HTML grid display by selecting either the first or last row of data, or rows adjacent to the current selection.</span></span>
>>>>>>> <span data-ttu-id="3c4e2-108">master</span><span class="sxs-lookup"><span data-stu-id="3c4e2-108">master</span></span>

## <a name="navigation-sub-procedures"></a><span data-ttu-id="3c4e2-109">Процедуры Sub навигации</span><span class="sxs-lookup"><span data-stu-id="3c4e2-109">Navigation Sub Procedures</span></span>

<span data-ttu-id="3c4e2-110">Приложение адресная книга содержит некоторые процедуры, которые позволяют пользователям щелкните **первый**, **Далее**, **Назад**и **последний** кнопки для перемещения данных.</span><span class="sxs-lookup"><span data-stu-id="3c4e2-110">The Address Book application contains several procedures that allow users to click the **First**, **Next**, **Previous**, and **Last** buttons to move around the data.</span></span>

<span data-ttu-id="3c4e2-111">Например, щелкнув **Первая** кнопка активирует первый VBScript\_процедуры OnClick Sub.</span><span class="sxs-lookup"><span data-stu-id="3c4e2-111">For example, clicking the **First** button activates the VBScript First\_OnClick Sub procedure.</span></span> <span data-ttu-id="3c4e2-112">Процедура выполняет метод [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) , что делает первую строку данных текущего выделенного фрагмента.</span><span class="sxs-lookup"><span data-stu-id="3c4e2-112">The procedure executes a [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) method, which makes the first row of data the current selection.</span></span> <span data-ttu-id="3c4e2-113">Нажатие кнопки **последней** активирует последний\_процедуры OnClick Sub, которая вызывает метод [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) текущего выделения последней строки данных.</span><span class="sxs-lookup"><span data-stu-id="3c4e2-113">Clicking the **Last** button activates the Last\_OnClick Sub procedure, which invokes the [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) method, making the last row of data the current selection.</span></span> <span data-ttu-id="3c4e2-114">Аналогичным образом работать оставшихся кнопок навигации.</span><span class="sxs-lookup"><span data-stu-id="3c4e2-114">The remaining navigation buttons work in a similar fashion.</span></span>

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

