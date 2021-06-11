---
title: QuickStyleLineColor Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dcfb792f-e02a-4059-acec-a178d221097c
description: Определяет цвет темы, который используется в строке фигуры, в виде integer от 0 до 7.
ms.openlocfilehash: 010b943f2266b1e0ee192e5f1341d73851d176fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437045"
---
# <a name="quickstylelinecolor-cell-quick-style-section"></a>QuickStyleLineColor Cell (Quick Style Section)

Определяет цвет темы, который используется в строке фигуры, в виде integer от 0 до 7.
  
|||
|:-----|:-----|
|Значение  <br/> |Описание  <br/> |
|0  <br/> |Цвет линии формы наследуется от цвета темной темы.  <br/> |
|1  <br/> |Цвет линии формы наследуется от цвета темы Light.  <br/> |
|2  <br/> |Цвет линии формы наследуется от цвета темы Accent 1  <br/> |
|3  <br/> |Цвет линии формы наследуется от цвета темы Accent 2  <br/> |
|4   <br/> |Цвет линии формы наследуется от цвета темы Accent 3  <br/> |
|5   <br/> |Цвет линии формы наследуется от цвета темы Accent 4  <br/> |
|6   <br/> |Цвет линии формы наследуется от цвета темы Accent 5  <br/> |
|7   <br/> |Цвет линии формы наследуется от цвета темы Accent 6  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на **ячейку QuickStyleLineColor** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы с использованием свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | QuickStyleLineColor  <br/> |
   
Чтобы получить ссылку на **ячейку QuickStyleLineColor** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowQuickStyleProperties** <br/> |
| Индекс ячейки:  <br/> |**visQuickStyleLineColor** <br/> |
   

