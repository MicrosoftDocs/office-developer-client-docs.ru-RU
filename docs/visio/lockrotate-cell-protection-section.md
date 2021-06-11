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
description: Блокирует 2-D фигуры, которые вращаются с помощью ручки поворота или команды вращать левые 90° или вращать правой 90°.
ms.openlocfilehash: 36da1868e4f974bd19d00e86e31bea96eb8ad5bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404675"
---
# <a name="lockrotate-cell-protection-section"></a>LockRotate Cell (Protection Section)

Блокирует 2-D фигуры, которые вращаются с помощью ручки поворота или команды вращать левые **90°** или вращать правой **90°.** 
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Фигура не может быть повернута.  <br/> |
| FALSE  <br/> | Фигура может быть повернута (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Примечания

Ячейка LockRotate не мешает вращать фигуру 1-D при перетаскивке конечной точки. Чтобы заблокировать 1-D-форму от вращения, установите ячейку LockWidth ненулевую величину (TRUE).
  
Чтобы получить ссылку на ячейку LockRotate по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LockRotate  <br/> |
   
Чтобы получить ссылку на ячейку LockRotate по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockRotate** <br/> |
   

