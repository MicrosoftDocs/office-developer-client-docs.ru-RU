---
title: Ячейка LockRotate (раздел "Защита")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm655
localization_priority: Normal
ms.assetid: 2d97b31d-9008-307d-273a-1726007eeb34
description: Блокирует плоских фигур с поворот с помощью маркера вращения или слева поворот 90° или 90° команду Поворот вправо.
ms.openlocfilehash: 450fe4786594472d018b705df4678fe636390ac3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814146"
---
# <a name="lockrotate-cell-protection-section"></a>Ячейка LockRotate (раздел "Защита")

Блокирует плоских фигур с поворот маркер вращения **Поворот левой 90 °** или **Поворот вправо 90 °** команды. 
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Не удается вращаться фигуры.  <br/> |
| FALSE  <br/> | Фигура может быть вращаться (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Замечания

Ячейка LockRotate не запрещает одномерной фигуры поворот при перетаскивании конечную точку. Блокировка одномерной фигуры от вращение значение ячейки LockWidth отличное от нуля значение (TRUE).
  
Чтобы получить ссылку на ячейку LockRotate по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LockRotate  <br/> |
   
Для получения ссылки на ячейки LockRotate по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockRotate** <br/> |
   

