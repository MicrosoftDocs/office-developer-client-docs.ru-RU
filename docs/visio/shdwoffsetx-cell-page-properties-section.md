---
title: ShdwOffsetX Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251373
localization_priority: Normal
ms.assetid: 92ec9b11-f53f-a1c9-832a-6cac08aa5379
description: Определяет расстояние в единицах страницы, на которое тень фигуры смещена по горизонтали от фигуры.
ms.openlocfilehash: fbc7d37fc8ba45f3219af6a4350301102954f23d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431654"
---
# <a name="shdwoffsetx-cell-page-properties-section"></a>ShdwOffsetX Cell (Page Properties Section)

Определяет расстояние в единицах страницы, на которое тень фигуры смещена по горизонтали от фигуры.
  
## <a name="remarks"></a>Примечания

Это значение устанавливается в диалоговом окне "Настройка страницы" (на вкладке "Конструктор" щелкните стрелку **"Настройка** страницы").   Это значение не зависит от масштаба рисунка. Если рисунок масштабирован, смещение теней остается таким же. 
  
Чтобы получить ссылку на ячейку ShdwOffsetX по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | ShdwOffsetX  <br/> |
   
Чтобы получить ссылку на ячейку ShdwOffsetX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPage** <br/> |
| Индекс ячейки:  <br/> |**visPageShdwOffsetX** <br/> |
   

