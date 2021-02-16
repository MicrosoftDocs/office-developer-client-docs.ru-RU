---
title: ThemeIndex Cell (Theme Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: Сохраняет в качестве всего 100 000 000 000 000 000 000 000 000 000 000 000 000 000 000 000 000 . Если для документа выбрана новая тема, ячейка ThemeIndex для документа, а также все страницы и фигуры, которые он содержит, обновляется с помощью индекса встроенной темы.
ms.openlocfilehash: 6ddede864a54fbd7127552499d3ee1ae3d36efc1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411913"
---
# <a name="themeindex-cell-theme-properties-section"></a>ThemeIndex Cell (Theme Properties Section)

Сохраняет в качестве всего 100 000 000 000 000 000 000 000 000 000 000 000 000 000 000 000 000 . Если для документа выбрана новая тема, ячейка **ThemeIndex** для документа, а также все страницы и фигуры, которые он содержит, обновляется с помощью индекса встроенной темы. 
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **ThemeIndex** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | ThemeIndex  <br/> |
   
Чтобы получить ссылку на ячейку **ThemeIndex** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowThemeProperties** <br/> |
| Индекс ячейки:  <br/> |**visThemeIndex** <br/> |
   

