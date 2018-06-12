---
title: Ячейка LockMoveY (раздел Защита)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm645
localization_priority: Normal
ms.assetid: 4ed8cab4-112a-e96a-f4e3-02490a6f87fa
description: Блокирует вертикальную позицию фигуры, чтобы он не перемещаться по вертикали.
ms.openlocfilehash: 24f6f477860ea3634cfdcfd92199f2de65e543db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814136"
---
# <a name="lockmovey-cell-protection-section"></a>Ячейка LockMoveY (раздел Защита)

Блокирует вертикальную позицию фигуры, чтобы он не перемещаться по вертикали.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Позиция по вертикали блокировки.  <br/> |
| FALSE  <br/> | Позиция по вертикали не блокируется.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку LockMoveY по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LockMoveY  <br/> |
   
Для получения ссылки на ячейки LockMoveY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockMoveY** <br/> |
   

