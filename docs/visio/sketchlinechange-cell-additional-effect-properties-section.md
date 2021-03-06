---
title: SketchLineChange Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: Определяет количество рандомизации линии фигуры из геометрии фигуры при использовании эффекта эскиза в процентах от длины раздела. Если значение ячейки SketchLineChange установлено до 0%, геометрия линии фигуры соответствует геометрии фигуры. Если значение 100%, геометрия линии фигуры не следует геометрии фигуры.
ms.openlocfilehash: ba57a4d2e43a91475f4c3ab4862f723eb2653a89
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419508"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a>SketchLineChange Cell (Additional Effect Properties Section)

Определяет количество рандомизации линии фигуры из геометрии фигуры при использовании эффекта эскиза в процентах от длины раздела. Если значение ячейки **SketchLineChange** установлено до 0%, геометрия линии фигуры соответствует геометрии фигуры. Если значение 100%, геометрия линии фигуры не следует геометрии фигуры. 
  
## <a name="remarks"></a>Примечания

Для наилучших результатов идеальный диапазон значений для ячейки **SketchLineChange** составляет от 15% до 50%. Значение ниже 15% едва заметно; значение, большее 50%, может слишком рандомизировать строку. 
  
Чтобы получить ссылку на ячейку **SketchLineChange** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы с использованием свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | SketchLineChange  <br/> |
   
Чтобы получить ссылку на **ячейку SketchLineChange** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowOtherEffectProperties** <br/> |
| Индекс ячейки:  <br/> |**visSketchLineChange** <br/> |
   

