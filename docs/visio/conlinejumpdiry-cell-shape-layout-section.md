---
title: Ячейка ConLineJumpDirY (раздел макет фигуры)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251654
localization_priority: Normal
ms.assetid: 93f82ae0-3442-fac1-9906-b84afef85f5c
description: Определяет направление пересечения линий при пересечении вертикальной динамической соединительной линии для фигуры.
ms.openlocfilehash: 2d0c0964b52c9afbccc9cb507024825434702b6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813446"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a>Ячейка ConLineJumpDirY (раздел макет фигуры)

Определяет направление пересечения линий при пересечении вертикальной динамической соединительной линии для фигуры.
  
|**Значение**|**Направление**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Страница по умолчанию  <br/> |**visLOJumpDirYDefault** <br/> |
| 1  <br/> | Слева  <br/> |**visLOJumpDirYLeft** <br/> |
| 2  <br/> | Правильно  <br/> |**visLOJumpDirYRight** <br/> |
   
## <a name="remarks"></a>Замечания

По умолчанию вертикали для *всех* соединителей переходит на страницу, использовать ячейку PageLineJumpDirY в разделе макет страницы. 
  
Чтобы получить ссылку на ячейку ConLineJumpDirY по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | ConLineJumpDirY  <br/> |
   
Для получения ссылки на ячейки ConLineJumpDirY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
| Индекс ячейки:  <br/> |**visSLOJumpDirY** <br/> |
   

