---
title: Ячейка TheText (раздел событий)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1005
localization_priority: Normal
ms.assetid: 2d63768e-afdb-4b3f-de49-f9ba69ae5391
description: Ячейка события, которое вычисляется при изменении текста или текста композиции фигуры.
ms.openlocfilehash: 942ccee4478c87243207d8d65785857758d2a068
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815025"
---
# <a name="thetext-cell-events-section"></a>Ячейка TheText (раздел событий)

Ячейка события, которое вычисляется при изменении текста или текста композиции фигуры.
  
## <a name="remarks"></a>Замечания

Событие ячеек вычисляются только в том случае, когда возникает событие, не после ввода формул. Можно использовать ячейку TheText для пересчета триггер, например для пересчета текст ширину и высоту с помощью функции (TEXTWIDTH) и TEXTHEIGHT ().
  
Чтобы получить ссылку на ячейку TheText по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | TheText  <br/> |
   
Для получения ссылки на ячейки TheText по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowEvent** <br/> |
| Индекс ячейки:  <br/> |**visEvtCellTheText** <br/> |
   

