---
title: LockHeight Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm635
localization_priority: Normal
ms.assetid: 218b957e-5af6-e53b-1453-a84164ae456e
description: Блокирует высоту фигуры таким образом, чтобы ее высота оставалась неизменной при повторном размере фигуры.
ms.openlocfilehash: 099f6597656d4389476818253f34e741ddd404de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432088"
---
# <a name="lockheight-cell-protection-section"></a>LockHeight Cell (Protection Section)

Блокирует высоту фигуры таким образом, чтобы ее высота оставалась неизменной при повторном размере фигуры.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Высота заблокирована.  <br/> |
| FALSE  <br/> | Высота не заблокирована.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку LockHeight по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LockHeight  <br/> |
   
Чтобы получить ссылку на ячейку LockHeight по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockHeight** <br/> |
   

