---
title: BevelTopType Cell (Bevel Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e29af0d-4183-41d1-8b0f-96450089f882
description: Определяет тип окантовки на верхнем краю фигуры.
ms.openlocfilehash: 225600a3e39ec58622bcd8597e1115a52cb62a3f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421496"
---
# <a name="beveltoptype-cell-bevel-properties-section"></a>BevelTopType Cell (Bevel Properties Section)

Определяет тип окантовки на верхнем краю фигуры. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Без bevel  <br/> |
|1  <br/> |Круг bevel  <br/> |
|2  <br/> |Relaxed Inset bevel  <br/> |
|3  <br/> |Cross bevel  <br/> |
|4   <br/> |Cool Slant bevel  <br/> |
|5   <br/> |Угловая гоголевка  <br/> |
|6   <br/> |Soft Round bevel  <br/> |
|7   <br/> |Выпукшная гоголевка  <br/> |
|8   <br/> |Спусковая пусковая дорожка  <br/> |
|9   <br/> |Divot bevel  <br/> |
|10   <br/> |Риблет-букель  <br/> |
|11  <br/> |Hard Edge bevel  <br/> |
|12   <br/> |Ар-деко bevel  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **BevelTopType** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |BevelTopType  <br/> |
   
Чтобы получить ссылку на ячейку **BevelTopType** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowBevelProperties** <br/> |
|Индекс ячейки:  <br/> |**visBevelTopType** <br/> |
   

