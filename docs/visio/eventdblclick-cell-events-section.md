---
title: Ячейка EventDblClick (раздел "События")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251312
localization_priority: Normal
ms.assetid: ca949013-f998-1bce-39e5-ac6f68ab2392
description: Ячейка события, которое вычисляется при двойном щелчке фигуры.
ms.openlocfilehash: 623d1d095d3269cd9c82fa8d0d6601933a163f92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813700"
---
# <a name="eventdblclick-cell-events-section"></a>Ячейка EventDblClick (раздел "События")

Ячейка события, которое вычисляется при двойном щелчке фигуры.
  
## <a name="remarks"></a>Замечания

Событие ячеек вычисляются только в том случае, когда возникает событие, не после ввода формул.
  
Чтобы получить ссылку на ячейку EventDblClick по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | EventDblClick  <br/> |
   
Для получения ссылки на ячейки EventDblClick по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowEvent** <br/> |
| Индекс ячейки:  <br/> |**visEvtCellDblClick** <br/> |
   

