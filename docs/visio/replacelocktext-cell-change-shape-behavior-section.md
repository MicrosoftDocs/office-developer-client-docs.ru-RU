---
title: ReplaceLockText Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: Указывает, переоформили ли значения указанных клеток в мастер-фигуре значения (в том числе локальные) фигуры, заменяемой во время операции замены фигуры. ReplaceLockText определяет, переопределяет ли текст, отображаемый на мастере, текст заменяемой фигуры.
ms.openlocfilehash: 299bd571ad935886879abb11108c3d0bd28e3183
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411920"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a>ReplaceLockText Cell (Change Shape Behavior Section)

Указывает, переоформили ли значения указанных клеток в мастер-фигуре значения (в том числе локальные) фигуры, заменяемой во время операции замены фигуры. **ReplaceLockText** определяет, переопределяет ли текст, отображаемый на мастере, текст заменяемой фигуры. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> | Текст на фигуре мастера переоформил текст на старую фигуру. Кроме того, во время операции замены фигуры мастер переоформит значения ячеек в следующих разделах:  <br/> **Раздел Текстовые поля**  <br/> **Раздел Формат блока текста**  <br/> |
|FALSE  <br/> |Форма замены содержит любые текстовые, текстовые поля или другие текстовые свойства из старой фигуры, добавленной в фигуру.  <br/> Когда форма замены содержит текстовые свойства из старой формы, форма замены также имеет значения из разделов **Символ** и Абзац старой формы, если они имеют несколько строк.   <br/> |
   
Если установлено значение TRUE (1), значения мастера фигуры заменяются значениями следующих значений на заменяемой фигуре:
  
- [TheText Cell (Events Section)](thetext-cell-events-section.md)
    
- Ячейки в [разделе Символ](character-section.md)
    
- Ячейки в [разделе Параграф](paragraph-section.md)
    
- Ячейки в [разделе Tabs](tabs-section.md)
    
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **ReplaceLockText** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы с использованием свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | ReplaceLockText  <br/> |
   
Чтобы получить ссылку на **ячейку ReplaceLockText** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowReplaceBehaviors** <br/> |
| Индекс ячейки:  <br/> |**visReplaceLockText** <br/> |
   

