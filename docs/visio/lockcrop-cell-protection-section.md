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
description: Блокирует объект из другой программы для кадрирования с помощью инструмента "рамка".
ms.openlocfilehash: bfb8bebd50908387fa3f94a8ca228935ef709133
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359628"
---
# <a name="lockcrop-cell-protection-section"></a>LockCrop Cell (Protection Section)

Блокирует объект из другой программы для кадрирования с помощью инструмента " **рамка** ". 
  
|**Value**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Не удается обрезать фигуру  <br/> |
| FALSE  <br/> | Фигуру можно обрезать.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку LockCrop по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LockCrop  <br/> |
   
Чтобы получить ссылку на ячейку LockCrop по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровлокк** <br/> |
| Индекс ячейки:  <br/> |**Вислокккроп** <br/> |
   

