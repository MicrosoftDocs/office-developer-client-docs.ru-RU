---
title: Ячейка EventXFMod (раздел "События")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251313
localization_priority: Normal
ms.assetid: b88588a2-c651-7eab-9c7a-ed78f20d1ba3
description: Ячейка события, которое вычисляется когда позиции или ориентации на странице фигуры преобразовать (XF).
ms.openlocfilehash: 5884aabc11798ae0440fbfa024b9cc2f2418b9cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813727"
---
# <a name="eventxfmod-cell-events-section"></a>Ячейка EventXFMod (раздел "События")

Ячейка события, которое вычисляется когда позиции или ориентации на странице фигуры преобразовать («XF»).
  
## <a name="remarks"></a>Замечания

Событие ячеек вычисляются только в том случае, когда возникает событие, не после ввода формул.
  
Чтобы получить ссылку на ячейку EventXFMod по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | EventXFMod  <br/> |
   
Для получения ссылки на ячейки EventXFMod по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowEvent** <br/> |
| Индекс ячейки:  <br/> |**visEvtCellXFMod** <br/> |
   

