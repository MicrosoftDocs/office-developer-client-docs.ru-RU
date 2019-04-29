---
title: LockVariation Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Определяет, можно ли изменить вариант темы, примененный к странице или фигуре, в виде логического значения.
ms.openlocfilehash: 69c991e3da7a96d6c59dc825dfb78fdad3d432e7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427929"
---
# <a name="lockvariation-cell-protection-section"></a>LockVariation Cell (Protection Section)

Определяет, можно ли изменить вариант темы, примененный к странице или фигуре, в виде логического значения.
  
|||
|:-----|:-----|
|TRUE  <br/> |Текущий вариант, примененный к странице или фигуре, не может быть изменен.  <br/> |
|FALSE  <br/> |Можно изменить вариант страницы или фигуры.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **LockVariation** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LockVariation  <br/> |
   
Чтобы получить ссылку на ячейку **LockVariation** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровлокк** <br/> |
| Индекс ячейки:  <br/> |**Вислокквариатион** <br/> |
   

