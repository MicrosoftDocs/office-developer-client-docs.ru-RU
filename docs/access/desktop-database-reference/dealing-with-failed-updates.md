---
title: Работа с ошибками обновлений
TOCTitle: Dealing with failed updates
ms:assetid: f6f4914d-59b3-f3f2-b986-218e07ce5a1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250258(v=office.15)
ms:contentKeyID: 48548752
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 659b5389074371ed4de41b909ab5228ad8fca080
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947751"
---
# <a name="dealing-with-failed-updates"></a><span data-ttu-id="0ba13-102">Работа с ошибками обновлений</span><span class="sxs-lookup"><span data-stu-id="0ba13-102">Dealing with failed updates</span></span>

<span data-ttu-id="0ba13-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0ba13-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="dealing-with-failed-updates"></a><span data-ttu-id="0ba13-104">Исправление неудачных обновлений</span><span class="sxs-lookup"><span data-stu-id="0ba13-104">Dealing with Failed Updates</span></span>

<span data-ttu-id="0ba13-105">Если обновление завершается с ошибками, способ устранения ошибки зависит от природы и уровень серьезности ошибки и логики приложения.</span><span class="sxs-lookup"><span data-stu-id="0ba13-105">When an update concludes with errors, how you resolve the errors depends on the nature and severity of the errors and the logic of your application.</span></span> <span data-ttu-id="0ba13-106">Тем не менее если база данных используется совместно с другими пользователями, типичные ошибки — это кто-либо изменяется поле перед выполнением.</span><span class="sxs-lookup"><span data-stu-id="0ba13-106">However, if the database is shared with other users, a typical error is that someone else modifies the field before you do.</span></span> <span data-ttu-id="0ba13-107">Этот тип ошибки называется *конфликта.*</span><span class="sxs-lookup"><span data-stu-id="0ba13-107">This type of error is called a *conflict.*</span></span> <span data-ttu-id="0ba13-108">ADO обнаруживает такие ситуации и сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="0ba13-108">ADO detects this situation and reports an error.</span></span>

<span data-ttu-id="0ba13-109">При наличии ошибок обновления, они будут содержатся в обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="0ba13-109">If there are update errors, they will be trapped in an error-handling routine.</span></span> <span data-ttu-id="0ba13-110">Фильтрация **записей** с константой **adFilterConflictingRecords** , чтобы были видны только конфликтующие строки.</span><span class="sxs-lookup"><span data-stu-id="0ba13-110">Filter the **Recordset** with the **adFilterConflictingRecords** constant so that only the conflicting rows are visible.</span></span> <span data-ttu-id="0ba13-111">В этом примере разрешение ошибок стратегия предназначена только для печати автора первого имени и фамилии (**au\_отображающее общие сведения** и **au\_lname**).</span><span class="sxs-lookup"><span data-stu-id="0ba13-111">In this example, the error-resolution strategy is merely to print the author's first and last names (**au\_fname** and **au\_lname**).</span></span>

<span data-ttu-id="0ba13-112">Код для предупреждения пользователя конфликт обновления выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0ba13-112">The code to alert the user to the update conflict looks like this:</span></span>

```vb 
 
objRs.Filter = adFilterConflictingRecords 
objRs.MoveFirst 
Do While Not objRst.EOF 
   Debug.Print "Conflict: Name =  "; objRs!au_fname; " "; objRs!au_lname 
   objRs.MoveNext 
Loop 
```

