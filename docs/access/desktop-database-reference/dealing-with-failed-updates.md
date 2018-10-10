---
title: Dealing with Failed Updates
TOCTitle: Dealing with Failed Updates
ms:assetid: f6f4914d-59b3-f3f2-b986-218e07ce5a1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250258(v=office.15)
ms:contentKeyID: 48548752
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d3af3026052954ec74b10026e0cf288a6aa5249
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480154"
---
# <a name="dealing-with-failed-updates"></a><span data-ttu-id="7c9ae-102">Dealing with Failed Updates</span><span class="sxs-lookup"><span data-stu-id="7c9ae-102">Dealing with Failed Updates</span></span>


<span data-ttu-id="7c9ae-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7c9ae-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="dealing-with-failed-updates"></a><span data-ttu-id="7c9ae-104">Dealing with Failed Updates</span><span class="sxs-lookup"><span data-stu-id="7c9ae-104">Dealing with Failed Updates</span></span>

<span data-ttu-id="7c9ae-105">Если обновление завершается с ошибками, способ устранения ошибки зависит от природы и уровень серьезности ошибки и логики приложения.</span><span class="sxs-lookup"><span data-stu-id="7c9ae-105">When an update concludes with errors, how you resolve the errors depends on the nature and severity of the errors and the logic of your application.</span></span> <span data-ttu-id="7c9ae-106">Тем не менее если база данных используется совместно с другими пользователями, типичные ошибки — это кто-либо изменяется поле перед выполнением.</span><span class="sxs-lookup"><span data-stu-id="7c9ae-106">However, if the database is shared with other users, a typical error is that someone else modifies the field before you do.</span></span> <span data-ttu-id="7c9ae-107">Этот тип ошибки называется *конфликта.*</span><span class="sxs-lookup"><span data-stu-id="7c9ae-107">This type of error is called a *conflict.*</span></span> <span data-ttu-id="7c9ae-108">ADO обнаруживает такие ситуации и сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="7c9ae-108">ADO detects this situation and reports an error.</span></span>

<span data-ttu-id="7c9ae-109">При наличии ошибок обновления, они будут содержатся в обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="7c9ae-109">If there are update errors, they will be trapped in an error-handling routine.</span></span> <span data-ttu-id="7c9ae-110">Фильтрация **записей** с константой **adFilterConflictingRecords** , чтобы были видны только конфликтующие строки.</span><span class="sxs-lookup"><span data-stu-id="7c9ae-110">Filter the **Recordset** with the **adFilterConflictingRecords** constant so that only the conflicting rows are visible.</span></span> <span data-ttu-id="7c9ae-111">В этом примере разрешение ошибок стратегия предназначена только для печати автора первого имени и фамилии (**au\_отображающее общие сведения** и **au\_lname**).</span><span class="sxs-lookup"><span data-stu-id="7c9ae-111">In this example, the error-resolution strategy is merely to print the author's first and last names (**au\_fname** and **au\_lname**).</span></span>

<span data-ttu-id="7c9ae-112">Код для предупреждения пользователя конфликт обновления выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7c9ae-112">The code to alert the user to the update conflict looks like this:</span></span>

```vb 
 
objRs.Filter = adFilterConflictingRecords 
objRs.MoveFirst 
Do While Not objRst.EOF 
   Debug.Print "Conflict: Name =  "; objRs!au_fname; " "; objRs!au_lname 
   objRs.MoveNext 
Loop 
```

