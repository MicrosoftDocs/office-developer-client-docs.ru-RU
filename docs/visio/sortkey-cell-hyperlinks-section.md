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
description: Число, определяющее порядок гиперссылок в контекстном меню.
ms.openlocfilehash: 002ab036f5305aa6daa631c15b0e9eb6148a9635
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406383"
---
# <a name="sortkey-cell-hyperlinks-section"></a>SortKey Cell (Hyperlinks Section)

Число, определяющее порядок гиперссылок в контекстном меню.
  
## <a name="remarks"></a>Примечания

Гиперссылки в контекстном меню отображаются в меню, отсортированном от самого низкого до более высокого, с меньшими номерами в верхней части меню. Если две строки гиперссылок имеют одинаковое значение ячейки SortKey, порядок определяется физическим порядком строк. Значение по умолчанию — 0 (ноль). 
  
Чтобы получить ссылку на ячейку SortKey по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Гиперссылки. *Name (имя* ). SortKey, где Hyperlink *. Name* — имя строки  <br/> |
   
Чтобы получить ссылку на ячейку SortKey по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**виссектионхиперлинк** <br/> |
|Индекс строки:  <br/> |**visRow1stHyperlink** +  *i* , где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**вишлинксорткэй** <br/> |
   

