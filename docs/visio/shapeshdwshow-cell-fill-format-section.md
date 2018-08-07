---
title: Ячейка ShapeShdwShow (раздел "Формат заливки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Определяет, будет ли фигуры тени, как целое число от 0 до 2.
ms.openlocfilehash: 72077e60089acd3cd3f8a9349691e1468f6b1f9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814798"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a>Ячейка ShapeShdwShow (раздел "Формат заливки")

Определяет, будет ли фигуры тени, как целое число от 0 до 2.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Всегда отображать тени, если указан тени. Теней в вложенные фигуры, не отображаются.  <br/> |
|1  <br/> |Не отображать тени, пока не имеет родительского узла фигуры. Используйте подменю фигура тени, если объединять.  <br/> |
|2  <br/> |Всегда отображать тень Если указан тени. Отображаются теней в вложенные фигуры.  <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки **ShapeShdwShow** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | ShapeShdwShow  <br/> |
   
Для получения ссылки на ячейки **ShapeShdwShow** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowFill** <br/> |
| Индекс ячейки:  <br/> |**visFillShdwShow** <br/> |
   

