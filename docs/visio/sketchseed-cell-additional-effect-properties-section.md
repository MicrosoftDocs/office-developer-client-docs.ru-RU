---
title: SketchSeed Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f62650d-36f8-4c6e-b79f-c9c397a5954d
description: Представляет значение случайности, используемого для определения геометрии эффекта наброска, в качестве положительного значения. Значение ячейки SketchSeed создается случайным образом, когда к фигуре применяется эффект наброска.
ms.openlocfilehash: 3ec58fbfa183d1a6d7bb6960672658f9a6cca073
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434398"
---
# <a name="sketchseed-cell-additional-effect-properties-section"></a>SketchSeed Cell (Additional Effect Properties Section)

Представляет значение случайности, используемого для определения геометрии эффекта наброска, в качестве положительного значения. Значение ячейки **SketchSeed** создается случайным образом, когда к фигуре применяется эффект наброска. 
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **SketchSeed** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | SketchSeed  <br/> |
   
Чтобы получить ссылку на ячейку **SketchSeed** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowOtherEffectProperties** <br/> |
| Индекс ячейки:  <br/> |**visSketchSeed** <br/> |
   

