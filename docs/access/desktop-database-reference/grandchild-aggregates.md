---
title: Статистические выражения на котором
TOCTitle: Grandchild aggregates
ms:assetid: ea5e2e1f-f3d5-f851-623a-a5d1385fe206
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250188(v=office.15)
ms:contentKeyID: 48548462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bc7576eb8e1555ab8b00d2800242c7be24baca58
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947940"
---
# <a name="grandchild-aggregates"></a>Статистические выражения на котором


**Применимо к**: Access 2013, Office 2013

Столбец главы, созданные в предложении команду фигуры может присваивается *имя псевдонима главы* (обычно с ключевым словом AS). Можно определить любого столбца в любой главы из формы **набора записей** с полным именем Идентификация дочерних, содержащую столбец. Например если главе родительского chap1, содержит дочерних главы, chap2, которая содержит столбец Сумма, сумма, а затем полным именем будет chap1.chap2.amt. Полное имя может использовать в качестве аргумента одному из агрегатных функций (SUM, AVG, MAX, MIN, COUNT, STDEV или какие-либо).

