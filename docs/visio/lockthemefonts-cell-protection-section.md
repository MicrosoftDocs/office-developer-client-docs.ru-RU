---
title: LockThemeFonts Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: Запрещает изменение ячейки Фонтиндекс в строке "свойства темы" путем применения новой темы. Не запрещает пользователям вручную изменять это значение в таблице свойств фигуры.
ms.openlocfilehash: b3bd21c1dcd8c8c13d843c50cb29edcc5b8c4999
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421230"
---
# <a name="lockthemefonts-cell-protection-section"></a>LockThemeFonts Cell (Protection Section)

Запрещает изменение ячейки **фонтиндекс** в строке " **свойства темы** " путем применения новой темы. Не запрещает пользователям вручную изменять это значение в таблице свойств фигуры. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Ячейка **фонтиндекс** не может быть изменена с текущим значением, если только таблица свойств не будет изменена напрямую.  <br/> |
|FALSE  <br/> |При изменении темы в ячейке **фонтиндекс** можно изменить ее текущее значение.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **LockThemeFonts** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LockThemeFonts  <br/> |
   
Чтобы получить ссылку на ячейку **LockThemeFonts** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровлокк** <br/> |
| Индекс ячейки:  <br/> |**Вислокксемефонтс** <br/> |
   

