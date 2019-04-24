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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292148"
---
# <a name="grandchild-aggregates"></a><span data-ttu-id="01722-102">Статистические выражения с внучатыми элементами</span><span class="sxs-lookup"><span data-stu-id="01722-102">Grandchild aggregates</span></span>


<span data-ttu-id="01722-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="01722-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="01722-104">Столбцу главы, созданному в выражении команды Shape, может быть присвоено *имя главы* (как правило, с помощью ключевого слова as).</span><span class="sxs-lookup"><span data-stu-id="01722-104">The chapter column created in a clause of a shape command may be given a *chapter-alias name* (typically with the AS keyword).</span></span> <span data-ttu-id="01722-105">Вы можете определить любой столбец в любой главе **набора записей** в форме, указав полное имя, идентифицирующее дочерний элемент, содержащий столбец.</span><span class="sxs-lookup"><span data-stu-id="01722-105">You may identify any column in any chapter of the shaped **Recordset** with a fully qualified name identifying the child containing the column.</span></span> <span data-ttu-id="01722-106">Например, если родительская глава, Chap1, содержит дочернюю главу, Chap2, которая содержит столбец Amount (сумма), то полное имя будет Chap1. Chap2. AMT. Полное имя затем можно использовать в качестве аргумента для одной из агрегатных функций (SUM, AVG, MAX, MIN, COUNT, STDEV или ANY).</span><span class="sxs-lookup"><span data-stu-id="01722-106">For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt. The qualified name may then be used as an argument to one of the aggregate functions (SUM, AVG, MAX, MIN, COUNT, STDEV, or ANY).</span></span>

