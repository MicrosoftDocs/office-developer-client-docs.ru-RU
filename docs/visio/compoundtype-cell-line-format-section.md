---
title: Ячейка CompoundType (раздел "Формат линий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: Определяет тип составные строки фигуры.
ms.openlocfilehash: 663b683030251c8b57324f1d2bdf492463c50eef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813431"
---
# <a name="compoundtype-cell-line-format-section"></a>Ячейка CompoundType (раздел "Формат линий")

Определяет тип составные строки фигуры. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Простое  <br/> |
|1  <br/> |Double  <br/> |
|2  <br/> |Жирная тонкая  <br/> |
|3  <br/> |Тонкая Жирная  <br/> |
|4  <br/> |Triple  <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки **CompoundType** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | CompoundType  <br/> |
   
Для получения ссылки на ячейки **CompoundType** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLine** <br/> |
| Индекс ячейки:  <br/> |**visCompoundType** <br/> |
   

