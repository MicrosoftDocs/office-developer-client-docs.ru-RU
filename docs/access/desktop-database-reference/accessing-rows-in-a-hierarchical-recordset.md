---
title: Доступ к строк в иерархической записей
TOCTitle: Accessing rows in a hierarchical Recordset
ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15)
ms:contentKeyID: 48548104
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: 3041aa1486f9630a36383dde4ad675c50c799339
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870032"
---
# <a name="accessing-rows-in-a-hierarchical-recordset"></a><span data-ttu-id="fe229-102">Доступ к строк в иерархической записей</span><span class="sxs-lookup"><span data-stu-id="fe229-102">Accessing rows in a hierarchical Recordset</span></span>

<span data-ttu-id="fe229-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe229-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fe229-104">В следующем примере показано действия, необходимые для доступа к строк в иерархической [набора записей](recordset-object-ado.md):</span><span class="sxs-lookup"><span data-stu-id="fe229-104">The following example shows the steps necessary to access rows in a hierarchical [Recordset](recordset-object-ado.md):</span></span>

1. <span data-ttu-id="fe229-105">Объекты **набора записей** из авторов и titleauthor таблицы связаны с идентификатором автора.</span><span class="sxs-lookup"><span data-stu-id="fe229-105">**Recordset** objects from the authors and titleauthor tables are related by author ID.</span></span>

2. <span data-ttu-id="fe229-106">Внешний цикл отображается имя и фамилию, состояние и идентификации каждого автора.</span><span class="sxs-lookup"><span data-stu-id="fe229-106">The outer loop displays each author's first and last name, state, and identification.</span></span>

3. <span data-ttu-id="fe229-107">Добавленный **набора записей** для каждой строки извлекается из коллекции **полей** и назначается *rstTitleAuthor*.</span><span class="sxs-lookup"><span data-stu-id="fe229-107">The appended **Recordset** for each row is retrieved from the **Fields** collection and assigned to *rstTitleAuthor*.</span></span>

4. <span data-ttu-id="fe229-108">Внутренний цикл отображаются четыре поля из каждой строки в присоединенной **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="fe229-108">The inner loop displays four fields from each row in the appended **Recordset**.</span></span>

> [!NOTE] 
> <span data-ttu-id="fe229-109">Свойство [StayInSync](stayinsync-property-ado.md) присвоено значение FALSE для наглядности, чтобы увидеть, главы явным образом изменить в каждой итерации внешнего цикла.</span><span class="sxs-lookup"><span data-stu-id="fe229-109">The [StayInSync](stayinsync-property-ado.md) property is set to FALSE for purposes of illustration, so you can see the chapter change explicitly in each iteration of the outer loop.</span></span> <span data-ttu-id="fe229-110">Тем не менее пример будет более эффективным, если назначение на шаге 3 перемещается перед первой строки на шаге 2, поэтому назначения выполняется только один раз.</span><span class="sxs-lookup"><span data-stu-id="fe229-110">However, the example will be more efficient if the assignment in step 3 is moved before the first line in step 2, so that the assignment is performed only once.</span></span> <span data-ttu-id="fe229-111">Присвойте свойству **StayInSync** значение TRUE, поэтому *rstTitleAuthor* неявно и автоматически изменится на соответствующий главы каждый раз, когда *rst* перемещает на новую строку.</span><span class="sxs-lookup"><span data-stu-id="fe229-111">Set the **StayInSync** property to TRUE, so that *rstTitleAuthor* will implicitly and automatically change to the corresponding chapter whenever *rst* moves to a new row.</span></span>

<span data-ttu-id="fe229-112">**Пример**</span><span class="sxs-lookup"><span data-stu-id="fe229-112">**Example**</span></span>

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

