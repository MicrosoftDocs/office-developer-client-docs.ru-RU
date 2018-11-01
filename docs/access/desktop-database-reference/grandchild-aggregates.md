---
title: Статистические выражения с внучатыми элементами
TOCTitle: Grandchild Aggregates
ms:assetid: ea5e2e1f-f3d5-f851-623a-a5d1385fe206
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250188(v=office.15)
ms:contentKeyID: 48548462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7c5ab45412b0524bcef14a952f5c5bbe0953278c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873532"
---
# <a name="grandchild-aggregates"></a>Статистические выражения с внучатыми элементами


**Применимо к**: Access 2013, Office 2013

Столбец главы, созданные в предложении команду фигуры может присваивается *имя псевдонима главы* (обычно с ключевым словом AS). Можно определить любого столбца в любой главы из формы **набора записей** с полным именем Идентификация дочерних, содержащую столбец. Например если главе родительского chap1, содержит дочерних главы, chap2, которая содержит столбец Сумма, сумма, а затем полным именем будет chap1.chap2.amt. Полное имя может использовать в качестве аргумента одному из агрегатных функций (SUM, AVG, MAX, MIN, COUNT, STDEV или какие-либо).

