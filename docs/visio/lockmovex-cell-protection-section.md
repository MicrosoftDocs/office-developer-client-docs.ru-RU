---
title: LockMoveX Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm640
localization_priority: Normal
ms.assetid: 48ceeeed-66ae-a81f-2aee-f0010102dfb7
description: Блокирует горизонтальное положение фигуры, поэтому ее невозможно по горизонтали.
ms.openlocfilehash: af0cee32370a540cd8d7aaf960cc0cbc27cc8f97
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435861"
---
# <a name="lockmovex-cell-protection-section"></a>LockMoveX Cell (Protection Section)

Блокирует горизонтальное положение фигуры, поэтому ее невозможно по горизонтали.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Горизонтальное положение заблокировано.  <br/> |
| FALSE  <br/> | Горизонтальное положение не заблокировано.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку LockMoveX по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LockMoveX  <br/> |
   
Чтобы получить ссылку на ячейку LockMoveX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockMoveX** <br/> |
   

