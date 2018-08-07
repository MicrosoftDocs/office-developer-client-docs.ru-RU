---
title: Ячейка EventDrop (раздел "События")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm350
localization_priority: Normal
ms.assetid: f84afe83-8391-0c13-f442-ea8794b38642
description: Ячейка события, которое оценивается при перетаскивании фигуры на странице документа как экземпляр или при дублировании или вставке фигуры.
ms.openlocfilehash: e2624c50896de061727003a48f7dc1559c6a72c4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813698"
---
# <a name="eventdrop-cell-events-section"></a>Ячейка EventDrop (раздел "События")

Ячейка события, которое оценивается при перетаскивании фигуры на странице документа как экземпляр или при дублировании или вставке фигуры.
  
## <a name="remarks"></a>Замечания

Событие ячеек вычисляются только в том случае, когда возникает событие, не после ввода формул.
  
Чтобы получить ссылку на ячейку EventDrop по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | EventDrop  <br/> |
   
Для получения ссылки на ячейки EventDrop по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowEvent** <br/> |
| Индекс ячейки:  <br/> |**visEvtCellDrop** <br/> |
   

