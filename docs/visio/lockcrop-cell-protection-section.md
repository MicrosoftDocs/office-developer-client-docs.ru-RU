---
title: LockCrop Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm610
localization_priority: Normal
ms.assetid: ae05de63-b527-66e6-2c79-056c9c92ec95
description: Блокирует объект из другой программы от обрезки средством обрезки.
ms.openlocfilehash: bfb8bebd50908387fa3f94a8ca228935ef709133
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411857"
---
# <a name="lockcrop-cell-protection-section"></a>LockCrop Cell (Protection Section)

Блокирует объект из другой программы от обрезки средством **обрезки.** 
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Фигуру невозможно обрезить  <br/> |
| FALSE  <br/> | Фигура может быть обрезана.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку LockCrop по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LockCrop  <br/> |
   
Чтобы получить ссылку на ячейку LockCrop по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockCrop** <br/> |
   

