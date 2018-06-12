---
title: Ячейка ConLineJumpDirX (раздел макет фигуры)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm185
localization_priority: Normal
ms.assetid: f0671835-8d48-907a-eca6-43953658f800
description: Определяет направление пересечения линий при пересечении горизонтальной динамической соединительной линии для фигуры.
ms.openlocfilehash: 396830d0da22c15f036f95808b3a94c33e9dc5bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813458"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a>Ячейка ConLineJumpDirX (раздел макет фигуры)

Определяет направление пересечения линий при пересечении горизонтальной динамической соединительной линии для фигуры.
  
|**Значение**|**Направление**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Страница по умолчанию  <br/> |**visLOJumpDirXDefault** <br/> |
| 1  <br/> | Вверх   <br/> |**visLOJumpDirXUp** <br/> |
| 2  <br/> | Вниз  <br/> |**visLOJumpDirXDown** <br/> |
   
## <a name="remarks"></a>Замечания

По умолчанию горизонтали для *всех* соединителей переходит на страницу, использовать ячейку PageLineJumpDirX в разделе макет страницы. 
  
Чтобы получить ссылку на ячейку ConLineJumpDirX по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | ConLineJumpDirX  <br/> |
   
Для получения ссылки на ячейки ConLineJumpDirX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
| Индекс ячейки:  <br/> |**visSLOJumpDirX** <br/> |
   

