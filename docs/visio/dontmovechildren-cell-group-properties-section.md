---
title: Ячейка DontMoveChildren (раздел "Свойства группы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm255
localization_priority: Normal
ms.assetid: ff5bbf05-4851-30ce-7ee1-f0ce7b2781ab
description: Определяет, будет ли перетаскивать фигуры в группы с помощью мыши.
ms.openlocfilehash: df5d0d2b44e283ee8301d9c088d3ce55114e9a75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813634"
---
# <a name="dontmovechildren-cell-group-properties-section"></a>Ячейка DontMoveChildren (раздел "Свойства группы")

Определяет, будет ли перетаскивать фигуры в группы с помощью мыши.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Не разрешать фигур в группе для переноса с помощью мыши.  <br/> |
| FALSE  <br/> | Разрешить фигур в группе для переноса с помощью мыши.  <br/> |
   
## <a name="remarks"></a>Замечания

Когда значение ячейки имеет значение TRUE, можно по-прежнему отражение, поворот, изменения размера или изменить положение фигур в группы, используя другие методы.
  
Значение ячейки имеет значение TRUE для групп в образцов и групп в экземпляры образцов, созданных в версиях Visio до версии 2000.
  
Чтобы получить ссылку на ячейку DontMoveChildren по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | DontMoveChildren  <br/> |
   
Для получения ссылки на ячейки DontMoveChildren по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowGroup** <br/> |
| Индекс ячейки:  <br/> |**visGroupDontMoveChildren** <br/> |
   

