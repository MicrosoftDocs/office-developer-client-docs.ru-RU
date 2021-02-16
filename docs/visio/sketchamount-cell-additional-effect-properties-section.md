---
title: SketchAmount Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Определяет искажение эффекта наброска в качестве количества от 0 до 25.
ms.openlocfilehash: fd9ee3390d05f24d81d9c6677160155b0f0f0d35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404423"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a>SketchAmount Cell (Additional Effect Properties Section)

Определяет искажение эффекта наброска в качестве количества от 0 до 25. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |К фигуре не применяется эффект наброска.  <br/> |
|1-25  <br/> |К фигуре применено искажение эскиза, где значение 1 является самым искажением, а 25 — наименьшим.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **SketchAmount** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | SketchAmount  <br/> |
   
Чтобы получить ссылку на ячейку **SketchAmount** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowOtherEffectProperties** <br/> |
| Индекс ячейки:  <br/> |**visSketchAmount** <br/> |
   

