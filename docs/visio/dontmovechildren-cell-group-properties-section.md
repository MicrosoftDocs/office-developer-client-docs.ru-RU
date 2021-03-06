---
title: DontMoveChildren Cell (Group Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm255
localization_priority: Normal
ms.assetid: ff5bbf05-4851-30ce-7ee1-f0ce7b2781ab
description: Определяет, можно ли перетаскивать фигуры в группе с помощью мыши.
ms.openlocfilehash: 2b15d75a98b5f5a72bce8b80758d27b197a346ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416596"
---
# <a name="dontmovechildren-cell-group-properties-section"></a>DontMoveChildren Cell (Group Properties Section)

Определяет, можно ли перетаскивать фигуры в группе с помощью мыши.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Не позволяйте перетаскивание фигур в группе с помощью мыши.  <br/> |
| FALSE  <br/> | Разрешить перетаскивание фигур в группе с помощью мыши.  <br/> |
   
## <a name="remarks"></a>Примечания

Когда значение этой ячейки true, вы все равно можете перевернуть, повернуть, изменить размер или изменить фигуры в группах с помощью других методов.
  
Значение этой ячейки true для групп в мастерах и группах в экземплярах мастеров, созданных в версиях Visio версии 2000.
  
Чтобы получить ссылку на ячейку DontMoveChildren по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | DontMoveChildren  <br/> |
   
Чтобы получить ссылку на ячейку DontMoveChildren по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowGroup** <br/> |
| Индекс ячейки:  <br/> |**visGroupDontMoveChildren** <br/> |
   

