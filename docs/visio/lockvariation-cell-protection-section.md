---
title: Ячейка LockVariation (раздел Защита)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Определяет, будет ли вариантов темы, применяются на страницу или форму можно изменить, как логическое значение.
ms.openlocfilehash: c3c272a637f28aa4df43f6c23030d6676280138e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814172"
---
# <a name="lockvariation-cell-protection-section"></a>Ячейка LockVariation (раздел Защита)

Определяет, будет ли вариантов темы, применяются на страницу или форму можно изменить, как логическое значение.
  
|||
|:-----|:-----|
|TRUE  <br/> |Нельзя изменить текущий вариантов, применяется к странице или фигуры.  <br/> |
|FALSE  <br/> |Можно изменить вариантов фигуры или страницы.  <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки **LockVariation** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LockVariation  <br/> |
   
Для получения ссылки на ячейки **LockVariation** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockVariation** <br/> |
   

