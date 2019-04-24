---
title: LockThemeIndex Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: Предотвращает изменение ячейки ThemeIndex в свойствах темы путем применения новой темы или выбора новой схемы соединителей. Не запрещает пользователям вручную изменять это значение в таблице свойств фигуры.
ms.openlocfilehash: 519c17f6e00c9aad2b5522bc66b41c0ceb75911b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358081"
---
# <a name="lockthemeindex-cell-protection-section"></a>LockThemeIndex Cell (Protection Section)

Предотвращает изменение ячейки **ThemeIndex** в **свойствах темы** путем применения новой темы или выбора новой схемы соединителей. Не запрещает пользователям вручную изменять это значение в таблице свойств фигуры. 
  
|**Value**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Ячейка **ThemeIndex** не может быть изменена с текущим значением, если только таблица свойств не будет изменена напрямую.  <br/> |
|FALSE  <br/> |При изменении темы в ячейке **ThemeIndex** можно изменить ее текущее значение.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **LockThemeIndex** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LockThemeIndex  <br/> |
   
Чтобы получить ссылку на ячейку **LockThemeIndex** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровлокк** <br/> |
| Индекс ячейки:  <br/> |**Вислокксемеиндекс** <br/> |
   

