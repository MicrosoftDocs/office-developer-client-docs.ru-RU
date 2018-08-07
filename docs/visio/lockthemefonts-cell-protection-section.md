---
title: Ячейка LockThemeFonts (раздел "Защита")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: Запрещает FontIndex ячейку в строке темы свойств изменяются, применение новой темы. Запрещает пользователям изменять это значение в таблице свойств фигуры вручную.
ms.openlocfilehash: b90ffe4c5555df017bb0506a78351514c954ec39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814176"
---
# <a name="lockthemefonts-cell-protection-section"></a>Ячейка LockThemeFonts (раздел "Защита")

Запрещает **FontIndex** ячейку в строке **Темы свойств** изменяются, применение новой темы. Запрещает пользователям изменять это значение в таблице свойств фигуры вручную. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Ячейка **FontIndex** может быть изменен с текущим значением только напрямую изменить в таблице свойств фигуры.  <br/> |
|FALSE  <br/> |Ячейка **FontIndex** могут изменяться с текущим значением при изменении темы.  <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки **LockThemeFonts** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LockThemeFonts  <br/> |
   
Для получения ссылки на ячейки **LockThemeFonts** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockThemeFonts** <br/> |
   

