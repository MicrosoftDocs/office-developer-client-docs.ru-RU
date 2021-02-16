---
title: QuickStyleFillColor Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 41250e47-404c-40e7-99be-9bb8c1ed5ba2
description: Определяет цвет темы, который использует заливка фигуры, в виде integer от 0 до 7
ms.openlocfilehash: 3ace0de7e3bfc878a2101eaca3847ef079b8f919
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407965"
---
# <a name="quickstylefillcolor-cell-quick-style-section"></a>QuickStyleFillColor Cell (Quick Style Section)

Определяет цвет темы, который использует заливка фигуры, в виде integer от 0 до 7
  
|||
|:-----|:-----|
|Значение  <br/> |Описание  <br/> |
|0  <br/> |Цвет заливки фигуры наследуется от цвета темной темы.  <br/> |
|1   <br/> |Цвет заливки фигуры наследуется от цвета светлой темы.  <br/> |
|2   <br/> |Цвет заливки фигуры наследуется от цвета темы Accent 1  <br/> |
|3   <br/> |Цвет заливки фигуры наследуется от цвета темы Accent 2  <br/> |
|4   <br/> |Цвет заливки фигуры наследуется от цвета темы Accent 3  <br/> |
|5   <br/> |Цвет заливки фигуры наследуется от цвета темы Accent 4  <br/> |
|6   <br/> |Цвет заливки фигуры наследуется от цвета темы Accent 5  <br/> |
|7   <br/> |Цвет заливки фигуры наследуется от цвета темы Accent 6  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **QuickStyleFillColor** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | QuickStyleFillColor  <br/> |
   
Чтобы получить ссылку на ячейку **QuickStyleFillColor** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowQuickStyleProperties** <br/> |
| Индекс ячейки:  <br/> |**visQuickStyleFillColor** <br/> |
   

