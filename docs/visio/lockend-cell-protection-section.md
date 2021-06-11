---
title: LockEnd Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm620
localization_priority: Normal
ms.assetid: e9742142-4d34-1ba9-480e-d1ecff4fc7cd
description: Блокирует конечную точку (EndX, EndY) 1-D-формы в определенное расположение.
ms.openlocfilehash: d9fe0372c44fe3b029a4d06056c8d3871c3f91e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425584"
---
# <a name="lockend-cell-protection-section"></a>LockEnd Cell (Protection Section)

Блокирует конечную точку (EndX, EndY) 1-D-формы в определенное расположение.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Конечная точка заблокирована.  <br/> |
| FALSE  <br/> | Конечная точка не заблокирована.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку LockEnd по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LockEnd  <br/> |
   
Чтобы получить ссылку на ячейку LockEnd по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockEnd** <br/> |
   

