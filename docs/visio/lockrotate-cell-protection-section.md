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
description: Блокирует поворачивать двухградивные фигуры с помощью вращающейся оси или команды Поворота влево на 90° или 90° вправо.
ms.openlocfilehash: 36da1868e4f974bd19d00e86e31bea96eb8ad5bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404675"
---
# <a name="lockrotate-cell-protection-section"></a>LockRotate Cell (Protection Section)

Блокирует поворачивать двухградивные фигуры с помощью вращающейся оси или команды Поворота влево **на 90°** или **90°** вправо. 
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Фигура не может быть повернута.  <br/> |
| FALSE  <br/> | Фигуру можно поворачивать (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Примечания

Ячейка LockRotate не препятствует повороту 1-D-фигуры при перетаскивке конечной точки. Чтобы заблокировать 1-D-фигуру от поворота, установите для ячейки LockWidth ненулевой значение (TRUE).
  
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
   

