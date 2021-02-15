---
title: Исправление неудачных обновлений
TOCTitle: Dealing with failed updates
ms:assetid: f6f4914d-59b3-f3f2-b986-218e07ce5a1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250258(v=office.15)
ms:contentKeyID: 48548752
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9a44548fd8747428b12c03c24207f36d3871e349
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294164"
---
# <a name="dealing-with-failed-updates"></a><span data-ttu-id="42dd1-102">Исправление неудачных обновлений</span><span class="sxs-lookup"><span data-stu-id="42dd1-102">Dealing with failed updates</span></span>

<span data-ttu-id="42dd1-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="42dd1-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="dealing-with-failed-updates"></a><span data-ttu-id="42dd1-104">Dealing with Failed Updates</span><span class="sxs-lookup"><span data-stu-id="42dd1-104">Dealing with Failed Updates</span></span>

<span data-ttu-id="42dd1-105">Когда обновление завершается ошибками, то то, как устранить ошибки, зависит от характера и серьезности ошибок и логики приложения.</span><span class="sxs-lookup"><span data-stu-id="42dd1-105">When an update concludes with errors, how you resolve the errors depends on the nature and severity of the errors and the logic of your application.</span></span> <span data-ttu-id="42dd1-106">Однако если база данных совместно используется другими пользователями, обычно ошибка в том, что кто-то другой изменяет поле до того, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="42dd1-106">However, if the database is shared with other users, a typical error is that someone else modifies the field before you do.</span></span> <span data-ttu-id="42dd1-107">Этот тип ошибки называется *конфликтом.*</span><span class="sxs-lookup"><span data-stu-id="42dd1-107">This type of error is called a *conflict.*</span></span> <span data-ttu-id="42dd1-108">ADO обнаруживает эту ситуацию и сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="42dd1-108">ADO detects this situation and reports an error.</span></span>

<span data-ttu-id="42dd1-109">Если имеются ошибки обновления, они будут захвачены в процедуру обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="42dd1-109">If there are update errors, they will be trapped in an error-handling routine.</span></span> <span data-ttu-id="42dd1-110">**Отфильтруем набор** записей с помощью константы **adFilterConflictingRecords,** чтобы были видны только конфликтующие строки.</span><span class="sxs-lookup"><span data-stu-id="42dd1-110">Filter the **Recordset** with the **adFilterConflictingRecords** constant so that only the conflicting rows are visible.</span></span> <span data-ttu-id="42dd1-111">В этом примере стратегия разрешения ошибок заключается только в печати первых и последних имен автора (**au \_ fname** и **au \_ lname).**</span><span class="sxs-lookup"><span data-stu-id="42dd1-111">In this example, the error-resolution strategy is merely to print the author's first and last names (**au\_fname** and **au\_lname**).</span></span>

<span data-ttu-id="42dd1-112">Код оповещения пользователя о конфликте обновлений выглядит так:</span><span class="sxs-lookup"><span data-stu-id="42dd1-112">The code to alert the user to the update conflict looks like this:</span></span>

```vb 
 
objRs.Filter = adFilterConflictingRecords 
objRs.MoveFirst 
Do While Not objRst.EOF 
   Debug.Print "Conflict: Name =  "; objRs!au_fname; " "; objRs!au_lname 
   objRs.MoveNext 
Loop 
```

