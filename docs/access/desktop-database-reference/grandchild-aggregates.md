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
# <a name="grandchild-aggregates"></a>Статистические выражения с внучатыми элементами


**Область применения**: Access 2013, Office 2013

Столбец главы, созданный в пункте команды фигуры, может быть назван псевдонимом *chapter-alias* (как правило, с ключевым словом AS). Вы можете идентифицировать любой столбец в любой главе фигурного набора **записей** с полностью квалифицированным именем, идентифицируя ребенка, содержащего столбец. Например, если в родительской главе chap1 содержится детская глава chap2, которая содержит столбец суммы, амт, то квалифицированным именем будет chap1.chap2.amt. Затем квалифицированное имя может использоваться в качестве аргумента для одной из совокупных функций (SUM, AVG, MAX, MIN, COUNT, STDEV или ANY).

