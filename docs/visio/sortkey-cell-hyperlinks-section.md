---
title: Ячейка SortKey (раздел "Гиперссылки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60086
localization_priority: Normal
ms.assetid: 93d7b00c-bd34-6b4e-44fe-afeb8aa9a294
description: Число, определяющее порядок гиперссылки, которые отображаются в контекстном меню.
ms.openlocfilehash: 03596918924b04a776eb7ffd2f16db1c57de8194
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814924"
---
# <a name="sortkey-cell-hyperlinks-section"></a>Ячейка SortKey (раздел "Гиперссылки")

Число, определяющее порядок гиперссылки, которые отображаются в контекстном меню.
  
## <a name="remarks"></a>Замечания

В меню Упорядочить от низшего к наибольшим, с нижней номера отображаются в верхней части меню отображаются гиперссылки в контекстном меню. Если две строки гиперссылки имеют такое же значение ячейки SortKey, порядок определяется порядок физических строк. Значение по умолчанию — нуль (0). 
  
Чтобы получить ссылку на ячейку SortKey по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |Гиперссылки. *имя* . SortKey, где гиперссылки *.name* — это имя строки  <br/> |
   
Для получения ссылки на ячейки SortKey по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionHyperlink** <br/> |
|Индекс строки:  <br/> |**visRow1stHyperlink** +  *i* где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visHLinkSortKey** <br/> |
   

