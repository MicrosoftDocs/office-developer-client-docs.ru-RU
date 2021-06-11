---
title: SortKey Cell (Hyperlinks Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60086
localization_priority: Normal
ms.assetid: 93d7b00c-bd34-6b4e-44fe-afeb8aa9a294
description: Номер, определяя порядок гиперссылки, которые отображаются в меню ярлыков.
ms.openlocfilehash: 002ab036f5305aa6daa631c15b0e9eb6148a9635
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406383"
---
# <a name="sortkey-cell-hyperlinks-section"></a>SortKey Cell (Hyperlinks Section)

Номер, определяя порядок гиперссылки, которые отображаются в меню ярлыков.
  
## <a name="remarks"></a>Примечания

Гиперссылки в меню ярлыка отображаются в меню, отсортировали от самого низкого до самого высокого, а в верхней части меню отображаются более низкие числа. Если две строки гиперссылки имеют одинаковое значение ячейки SortKey, порядок определяется физическим порядком строки. По умолчанию значение 0 (ноль). 
  
Чтобы получить ссылку на ячейку SortKey по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Гиперссылка. *имя*  . SortKey, где  *Hyperlink .name*  — это имя строки  <br/> |
   
Чтобы получить ссылку на ячейку SortKey по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionHyperlink** <br/> |
|Индекс строки:  <br/> |**visRow1stHyperlink**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
|Индекс ячейки:  <br/> |**visHLinkSortKey** <br/> |
   

