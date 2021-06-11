---
title: SketchFillChange Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Определяет количество рандомизации заполнения фигуры из геометрии фигуры при использовании эффекта эскиза в процентах от длины раздела. Если значение ячейки SketchFillChange установлено до 0%, то геометрия заполнения формы соответствует геометрии фигуры. Если значение 100%, ограниченная геометрия заполнения фигуры не следует геометрии фигуры.
ms.openlocfilehash: 8726e9dd6ca6257fb8dbbbef3dce1d4ec344e28b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408077"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a>SketchFillChange Cell (Additional Effect Properties Section)

Определяет количество рандомизации заполнения фигуры из геометрии фигуры при использовании эффекта эскиза в процентах от длины раздела. Если значение ячейки **SketchFillChange** установлено до 0%, то геометрия заполнения формы соответствует геометрии фигуры. Если значение 100%, ограниченная геометрия заполнения фигуры не следует геометрии фигуры. 
  
## <a name="remarks"></a>Примечания

Для наилучших результатов идеальный диапазон значений для ячейки **SketchFillChange** составляет от 15% до 50%. Значение ниже 15% едва заметно; значение, большее 50%, становится все более рандомизированным. 
  
Чтобы получить ссылку на ячейку **SketchFillChange** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы с использованием свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | SketchFillChange  <br/> |
   
Чтобы получить ссылку на ячейку **SketchFillChange** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowOtherEffectProperties** <br/> |
| Индекс ячейки:  <br/> |**visSketchFillChange** <br/> |
   

