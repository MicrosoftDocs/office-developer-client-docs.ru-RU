---
title: LockThemeIndex Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: Предотвращает изменение ячейки ThemeIndex в строке Свойства темы путем применения новой темы или выбора новой схемы соединителя. Не мешает пользователям вручную изменять это значение в ShapeSheet.
ms.openlocfilehash: 519c17f6e00c9aad2b5522bc66b41c0ceb75911b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411241"
---
# <a name="lockthemeindex-cell-protection-section"></a>LockThemeIndex Cell (Protection Section)

Предотвращает изменение **ячейки ThemeIndex** в строке **Свойства** темы путем применения новой темы или выбора новой схемы соединителя. Не мешает пользователям вручную изменять это значение в ShapeSheet. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Ячейка **ThemeIndex** не может быть изменена с текущего значения, если она не будет изменена непосредственно в ShapeSheet.  <br/> |
|FALSE  <br/> |Ячейка **ThemeIndex** может быть изменена с текущего значения при смене темы.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **LockThemeIndex** по имени из другой формулы, по значению **атрибута N** элемента **Cell** или из программы с использованием свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LockThemeIndex  <br/> |
   
Чтобы получить ссылку на ячейку **LockThemeIndex** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockThemeIndex** <br/> |
   

