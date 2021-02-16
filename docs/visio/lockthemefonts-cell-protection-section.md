---
title: LockThemeFonts Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: Предотвращает изменение ячейки FontIndex в строке "Свойства темы" путем применения новой темы. Не мешает пользователям вручную редактировать это значение в таблице shapeSheet.
ms.openlocfilehash: b3bd21c1dcd8c8c13d843c50cb29edcc5b8c4999
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421230"
---
# <a name="lockthemefonts-cell-protection-section"></a>LockThemeFonts Cell (Protection Section)

Предотвращает изменение **ячейки FontIndex** в строке **"Свойства** темы" путем применения новой темы. Не мешает пользователям вручную редактировать это значение в таблице shapeSheet. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Ячейку **FontIndex** нельзя изменить с текущего значения, если она не изменена непосредственно в shapeSheet.  <br/> |
|FALSE  <br/> |При смене темы ячейку **FontIndex** можно изменить с текущего значения.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **LockThemeFonts** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LockThemeFonts  <br/> |
   
Чтобы получить ссылку на ячейку **LockThemeFonts** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockThemeFonts** <br/> |
   

