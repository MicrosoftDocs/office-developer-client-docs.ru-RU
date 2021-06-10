---
title: Доступ к строкам в иерархическом наборе записей
TOCTitle: Accessing rows in a hierarchical Recordset
ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15)
ms:contentKeyID: 48548104
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a80b089fa72ef01eb1b4b2f1dae494e002c6a6fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281958"
---
# <a name="accessing-rows-in-a-hierarchical-recordset"></a><span data-ttu-id="85331-102">Доступ к строкам в иерархическом наборе записей</span><span class="sxs-lookup"><span data-stu-id="85331-102">Accessing rows in a hierarchical Recordset</span></span>

<span data-ttu-id="85331-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="85331-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="85331-104">В следующем примере показаны действия, необходимые для доступа к строкам в иерархическом [наборе записей:](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="85331-104">The following example shows the steps necessary to access rows in a hierarchical [Recordset](recordset-object-ado.md):</span></span>

1. <span data-ttu-id="85331-105">**Объекты Recordset** из таблиц авторов и titleauthor связаны с ИД автора.</span><span class="sxs-lookup"><span data-stu-id="85331-105">**Recordset** objects from the authors and titleauthor tables are related by author ID.</span></span>

2. <span data-ttu-id="85331-106">Внешний цикл отображает имя и фамилию каждого автора, состояние и идентификацию.</span><span class="sxs-lookup"><span data-stu-id="85331-106">The outer loop displays each author's first and last name, state, and identification.</span></span>

3. <span data-ttu-id="85331-107">Приложение **Recordset** для каждой строки извлекается из коллекции **Fields** и назначено *rstTitleAuthor.*</span><span class="sxs-lookup"><span data-stu-id="85331-107">The appended **Recordset** for each row is retrieved from the **Fields** collection and assigned to *rstTitleAuthor*.</span></span>

4. <span data-ttu-id="85331-108">Внутренний цикл отображает четыре поля из каждой строки в приложении **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="85331-108">The inner loop displays four fields from each row in the appended **Recordset**.</span></span>

> [!NOTE] 
> <span data-ttu-id="85331-109">Свойство [StayInSync](stayinsync-property-ado.md) настроено как FALSE для иллюстрации, поэтому в каждой итерации внешней петли можно увидеть явное изменение главы.</span><span class="sxs-lookup"><span data-stu-id="85331-109">The [StayInSync](stayinsync-property-ado.md) property is set to FALSE for purposes of illustration, so you can see the chapter change explicitly in each iteration of the outer loop.</span></span> <span data-ttu-id="85331-110">Однако пример будет более эффективным, если назначение на шаге 3 перемещается перед первой строкой на шаге 2, так что назначение выполняется только один раз.</span><span class="sxs-lookup"><span data-stu-id="85331-110">However, the example will be more efficient if the assignment in step 3 is moved before the first line in step 2, so that the assignment is performed only once.</span></span> <span data-ttu-id="85331-111">Установите **свойство StayInSync** true, чтобы *rstTitleAuthor* неявно и автоматически менял соответствующую главу всякий раз, когда *rST* перемещается в новую строку.</span><span class="sxs-lookup"><span data-stu-id="85331-111">Set the **StayInSync** property to TRUE, so that *rstTitleAuthor* will implicitly and automatically change to the corresponding chapter whenever *rst* moves to a new row.</span></span>

<span data-ttu-id="85331-112">**Пример**</span><span class="sxs-lookup"><span data-stu-id="85331-112">**Example**</span></span>

```vb 
 
Sub datashape() 
 Dim cnn As New ADODB.Connection 
 Dim rst As New ADODB.Recordset 
 Dim rstTitleAuthor As New ADODB.Recordset 
 
 cnn.Provider = "MSDataShape" 
 cnn.Open "Data Provider=MSDASQL;" & _ 
 "Data Source=SRV;" & _ 
 "User Id=MyUserName;Password=MyPassword;Database=Pubs" 
' STEP 1 
 rst.StayInSync = FALSE 
 rst.Open "SHAPE {select * from authors} " & _ 
 "APPEND ({select * from titleauthor} " & _ 
 "RELATE au_id TO au_id) AS chapTitleAuthor", _ 
 cnn 
' STEP 2 
 While Not rst.EOF 
 Debug.Print rst("au_fname"), rst("au_lname"), _ 
 rst("state"), rst("au_id") 
' STEP 3 
 Set rstTitleAuthor = rst("chapTitleAuthor").Value 
' STEP 4 
 While Not rstTitleAuthor.EOF 
 Debug.Print rstTitleAuthor(0), rstTitleAuthor(1), _ 
 rstTitleAuthor(2), rstTitleAuthor(3) 
 rstTitleAuthor.MoveNext 
 Wend 
 rst.MoveNext 
 Wend 
End Sub 
```

