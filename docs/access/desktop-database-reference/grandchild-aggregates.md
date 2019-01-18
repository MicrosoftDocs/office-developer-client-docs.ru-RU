---
title: Статистические выражения с внучатыми элементами
TOCTitle: Grandchild aggregates
ms:assetid: ea5e2e1f-f3d5-f851-623a-a5d1385fe206
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250188(v=office.15)
ms:contentKeyID: 48548462
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4c50898626488f909616977c6bb50c936434563
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722160"
---
# <a name="grandchild-aggregates"></a><span data-ttu-id="48d81-102">Статистические выражения с внучатыми элементами</span><span class="sxs-lookup"><span data-stu-id="48d81-102">Grandchild aggregates</span></span>


<span data-ttu-id="48d81-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="48d81-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="48d81-104">Столбец главы, созданные в предложении команду фигуры может присваивается *имя псевдонима главы* (обычно с ключевым словом AS).</span><span class="sxs-lookup"><span data-stu-id="48d81-104">The chapter column created in a clause of a shape command may be given a *chapter-alias name* (typically with the AS keyword).</span></span> <span data-ttu-id="48d81-105">Можно определить любого столбца в любой главы из формы **набора записей** с полным именем Идентификация дочерних, содержащую столбец.</span><span class="sxs-lookup"><span data-stu-id="48d81-105">You may identify any column in any chapter of the shaped **Recordset** with a fully qualified name identifying the child containing the column.</span></span> <span data-ttu-id="48d81-106">Например если главе родительского chap1, содержит дочерних главы, chap2, которая содержит столбец Сумма, сумма, а затем полным именем будет chap1.chap2.amt. Полное имя может использовать в качестве аргумента одному из агрегатных функций (SUM, AVG, MAX, MIN, COUNT, STDEV или какие-либо).</span><span class="sxs-lookup"><span data-stu-id="48d81-106">For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt. The qualified name may then be used as an argument to one of the aggregate functions (SUM, AVG, MAX, MIN, COUNT, STDEV, or ANY).</span></span>

