---
title: Ячейка LockThemeIndex (раздел "Защита")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: Запрещает ThemeIndex ячейка в строке темы свойств изменяются применение новой темы или выбрать новую схему соединителя. Запрещает пользователям изменять это значение в таблице свойств фигуры вручную.
ms.openlocfilehash: 4bef3eb799c943ff89027e69ae8580c9c0e51243
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814158"
---
# <a name="lockthemeindex-cell-protection-section"></a>Ячейка LockThemeIndex (раздел "Защита")

Запрещает **ThemeIndex** ячейка в строке **Темы свойств** изменяются применение новой темы или выбрать новую схему соединителя. Запрещает пользователям изменять это значение в таблице свойств фигуры вручную. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Ячейка **ThemeIndex** может быть изменен с текущим значением только напрямую изменить в таблице свойств фигуры.  <br/> |
|FALSE  <br/> |Ячейка **ThemeIndex** могут изменяться с текущим значением при изменении темы.  <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки **LockThemeIndex** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LockThemeIndex  <br/> |
   
Для получения ссылки на ячейки **LockThemeIndex** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockThemeIndex** <br/> |
   

