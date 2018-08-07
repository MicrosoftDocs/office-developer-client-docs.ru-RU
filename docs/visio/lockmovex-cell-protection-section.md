---
title: Ячейка LockMoveX (раздел "Защита")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm640
localization_priority: Normal
ms.assetid: 48ceeeed-66ae-a81f-2aee-f0010102dfb7
description: Блокирует горизонтальную позицию фигуры, чтобы он не перемещаться по горизонтали.
ms.openlocfilehash: 981f4f417e48f70d0693e30683c4351d0e53a758
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814154"
---
# <a name="lockmovex-cell-protection-section"></a>Ячейка LockMoveX (раздел "Защита")

Блокирует горизонтальную позицию фигуры, чтобы он не перемещаться по горизонтали.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Позиция по горизонтали блокировки.  <br/> |
| FALSE  <br/> | Позиция по горизонтали не блокируется.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку LockMoveX по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LockMoveX  <br/> |
   
Для получения ссылки на ячейки LockMoveX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockMoveX** <br/> |
   

