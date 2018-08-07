---
title: Ячейка ReplaceCopyCells (раздел "Изменение поведения фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: Указывает список ячеек в таблице свойств фигуры, которые копируются из старой фигуры фигуры замещения во время операции замены фигуры.
ms.openlocfilehash: 1e3b5e4dbc29372f75b7a7ed8013a7dd82d94e1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814566"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a>Ячейка ReplaceCopyCells (раздел "Изменение поведения фигуры")

Указывает список ячеек в таблице свойств фигуры, которые копируются из старой фигуры фигуры замещения во время операции замены фигуры. 
  
## <a name="remarks"></a>Замечания

Основной фигуры замены должно содержать вызов функции **DEPENDSON** в ячейке **ReplaceCopyCells** , где каждый аргумент в функцию — это ссылка на ячейку. Эти ячейки копируются из старой фигуры в фигуру, результатом операции замены фигуры, независимо от того, где они находятся в таблице свойств фигуры. 
  
Результирующая фигура копируются значения и/или формулы, ссылающиеся на другие ячейки. Если результирующая фигура не имеет связанной ячейки, скопированные ячейки содержит только значение. 
  
Ссылки в ячейке **ReplaceCopyCells** переопределить set защиты для ячеек, определенных в разделе **Защита** и **ReplaceLockFormat**, **ReplaceLockShapeData**и **ReplaceLockText** ячеек. 
  
Для получения ссылки на ячейки **ReplaceCopyCells** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | ReplaceCopyCells  <br/> |
   
Для получения ссылки на ячейки **ReplaceCopyCells** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowReplaceBehaviors** <br/> |
| Индекс ячейки:  <br/> |**visReplaceCopyCells** <br/> |
   

