---
title: LockRotate Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm655
localization_priority: Normal
ms.assetid: 2d97b31d-9008-307d-273a-1726007eeb34
description: Отменяет поворот плоских фигур с помощью маркера вращения или поворота влево на 90 ° или повернуть вправо 90 °.
ms.openlocfilehash: 36da1868e4f974bd19d00e86e31bea96eb8ad5bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404675"
---
# <a name="lockrotate-cell-protection-section"></a>LockRotate Cell (Protection Section)

Отменяет поворот плоских фигур с помощью маркера вращения или поворота **влево на 90 °** или **повернуть вправо 90 °** . 
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Поворот фигуры невозможен.  <br/> |
| FALSE  <br/> | Фигура может быть повернута (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Примечания

Ячейка LockRotate не предотвращает повернутую фигуру 1-D при перетаскивании конечной точки. Чтобы заблокировать одномерное фигуру относительно вращения, установите для ячейки LockWidth значение, отличное от нуля (TRUE).
  
Чтобы получить ссылку на ячейку LockRotate по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LockRotate  <br/> |
   
Чтобы получить ссылку на ячейку LockRotate по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**висровлокк** <br/> |
| Индекс ячейки:  <br/> |**вислоккротате** <br/> |
   

