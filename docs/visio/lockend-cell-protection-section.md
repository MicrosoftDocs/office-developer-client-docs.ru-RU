---
title: Ячейка LockEnd (раздел Защита)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm620
localization_priority: Normal
ms.assetid: e9742142-4d34-1ba9-480e-d1ecff4fc7cd
description: Блокирует конечную точку (КонецX, КонецY) одномерной фигуры в определенное расположение.
ms.openlocfilehash: d29f07e5b4b77ed2fb8b104769a2fdca55abcc8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814131"
---
# <a name="lockend-cell-protection-section"></a>Ячейка LockEnd (раздел Защита)

Блокирует конечную точку (КонецX, КонецY) одномерной фигуры в определенное расположение.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Конечная точка блокировки.  <br/> |
| FALSE  <br/> | Конечная точка не блокируется.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку LockEnd по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LockEnd  <br/> |
   
Для получения ссылки на ячейки LockEnd по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockEnd** <br/> |
   

