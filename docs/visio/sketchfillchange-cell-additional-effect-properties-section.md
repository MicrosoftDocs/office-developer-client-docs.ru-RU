---
title: SketchFillChange Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Определяет объем случайного выбора заливки фигуры из геометрии фигуры при использовании эффекта наброска в процентах от длины раздела. Если значение ячейки SketchFillChange составляет 0 %, вязая геометрия заливки фигуры соответствует геометрии фигуры. Если значение составляет 100 %, ограниченная геометрия заливки фигуры не следует за геометрией фигуры.
ms.openlocfilehash: 8726e9dd6ca6257fb8dbbbef3dce1d4ec344e28b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408077"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a>SketchFillChange Cell (Additional Effect Properties Section)

Определяет объем случайного выбора заливки фигуры из геометрии фигуры при использовании эффекта наброска в процентах от длины раздела. Если значение ячейки **SketchFillChange** — 0 %, то ограниченная геометрия заливки фигуры соответствует геометрии фигуры. Если значение составляет 100 %, ограниченная геометрия заливки фигуры не следует за геометрией фигуры. 
  
## <a name="remarks"></a>Примечания

Для наилучших результатов идеальный диапазон значений для ячейки **SketchFillChange** находится в диапазоне от 15% до 50%. Значение ниже 15 % почти не заметно; Значение больше 50% все чаще случайным образом. 
  
Чтобы получить ссылку на ячейку **SketchFillChange** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | SketchFillChange  <br/> |
   
Чтобы получить ссылку на ячейку **SketchFillChange** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowOtherEffectProperties** <br/> |
| Индекс ячейки:  <br/> |**visSketchFillChange** <br/> |
   

