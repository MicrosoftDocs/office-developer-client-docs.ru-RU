---
title: Ячейка SketchAmount (раздел "Дополнительные свойства эффекта")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Определяет объем искажений эффект эскиза, как целое число от 0 до 25.
ms.openlocfilehash: d5ae954f2eab48722c48c9bc4b3f640403dbb3ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814879"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a>Ячейка SketchAmount (раздел "Дополнительные свойства эффекта")

Определяет объем искажений эффект эскиза, как целое число от 0 до 25. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Фигура не действует эскиза применяется к нему.  <br/> |
|1-25  <br/> |Фигура имеет искажений эскиза применяется к нему, где значение 1: большинство искажений и 25 – меньше всего.  <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки **SketchAmount** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | SketchAmount  <br/> |
   
Для получения ссылки на ячейки **SketchAmount** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowOtherEffectProperties** <br/> |
| Индекс ячейки:  <br/> |**visSketchAmount** <br/> |
   

