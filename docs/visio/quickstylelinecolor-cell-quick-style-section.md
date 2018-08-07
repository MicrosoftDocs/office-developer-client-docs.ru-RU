---
title: Ячейка QuickStyleLineColor (раздел "Экспресс-стиль")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dcfb792f-e02a-4059-acec-a178d221097c
description: Определяет, какой цвет темы, которая использует строки фигуры, как целое число от 0 до 7.
ms.openlocfilehash: 2a660472998ade8148e8b70a3c6e4fc5fb3f4820
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814530"
---
# <a name="quickstylelinecolor-cell-quick-style-section"></a>Ячейка QuickStyleLineColor (раздел "Экспресс-стиль")

Определяет, какой цвет темы, которая использует строки фигуры, как целое число от 0 до 7.
  
|||
|:-----|:-----|
|Значение  <br/> |Описание  <br/> |
|0  <br/> |Цвет строки фигуры наследуется от темы темный цвет.  <br/> |
|1  <br/> |Цвет строки фигуры наследуется от цвет быстрое темы.  <br/> |
|2  <br/> |Цвет строки фигуры наследует от 1 контрастный цвет темы  <br/> |
|3  <br/> |Цвет строки фигуры наследует от 2 контрастный цвет темы  <br/> |
|4  <br/> |Цвет строки фигуры наследует от 3 контрастный цвет темы  <br/> |
|5  <br/> |Цвет строки фигуры наследует от 4 контрастный цвет темы  <br/> |
|6  <br/> |Цвет строки фигуры наследует от 5 контрастный цвет темы  <br/> |
|7  <br/> |Цвет строки фигуры наследует от 6 контрастный цвет темы  <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки **QuickStyleLineColor** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | QuickStyleLineColor  <br/> |
   
Для получения ссылки на ячейки **QuickStyleLineColor** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowQuickStyleProperties** <br/> |
| Индекс ячейки:  <br/> |**visQuickStyleLineColor** <br/> |
   

