---
title: QuickStyleShadowColor Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0a80959f-941f-451c-9049-dc661ff4930f
description: Определяет цвет темы, который использует тень фигуры, в виде integer от 0 до 7.
ms.openlocfilehash: b623eee89d214bade2706b12fcb344eccd8814b8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414958"
---
# <a name="quickstyleshadowcolor-cell-quick-style-section"></a>QuickStyleShadowColor Cell (Quick Style Section)

Определяет цвет темы, который использует тень фигуры, в виде integer от 0 до 7.
  
|||
|:-----|:-----|
|Значение  <br/> |Описание  <br/> |
|0  <br/> |Цвет тени формы наследуется от цвета темной темы.  <br/> |
|1  <br/> |Цвет тени формы наследуется от цвета темы Light.  <br/> |
|2  <br/> |Цвет теней формы наследуется от цвета темы Accent 1.  <br/> |
|3  <br/> |Цвет теней формы наследуется от цвета темы Accent 2.  <br/> |
|4   <br/> |Цвет теней формы наследуется от цвета темы Accent 3.  <br/> |
|5   <br/> |Цвет тени формы наследуется от цвета темы Accent 4.  <br/> |
|6   <br/> |Цвет теней формы наследуется от цвета темы Accent 5.  <br/> |
|7   <br/> |Цвет тени формы наследуется от цвета темы Accent 6.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на **ячейку QuickStyleShadowColor** по имени из другой формулы, по значению **атрибута N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | QuickStyleShadowColor  <br/> |
   
Чтобы получить ссылку на **ячейку QuickStyleShadowColor** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowQuickStyleProperties** <br/> |
| Индекс ячейки:  <br/> |**visQuickStyleShadowColor** <br/> |
   

