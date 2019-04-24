---
title: SketchAmount Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Определяет количество искажений для эффекты эскиза в виде целого числа от 0 до 25.
ms.openlocfilehash: fd9ee3390d05f24d81d9c6677160155b0f0f0d35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314772"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a>SketchAmount Cell (Additional Effect Properties Section)

Определяет количество искажений для эффекты эскиза в виде целого числа от 0 до 25. 
  
|**Value**|**Описание**|
|:-----|:-----|
|нуль  <br/> |К фигуре не применены эффекты эскиза.  <br/> |
|1-25  <br/> |К фигуре применено искажение эскизов, где значение 1 является самым подмножеством искажений, а 25 — наименьшей.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку **SketchAmount** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | SketchAmount  <br/> |
   
Чтобы получить ссылку на ячейку **SketchAmount** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровосереффектпропертиес** <br/> |
| Индекс ячейки:  <br/> |**Висскетчамаунт** <br/> |
   

