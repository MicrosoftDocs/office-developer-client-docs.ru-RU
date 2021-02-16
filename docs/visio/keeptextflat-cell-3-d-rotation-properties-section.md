---
title: KeepTextFlat Cell (3-D Rotation Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Указывает, будет ли текст фигуры игнорировать поворот фигуры в 3-D. Не применяется к 2-D повороту.
ms.openlocfilehash: fc8cf2fac431645876c7f81ed9864cb6c2036169
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422042"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a>KeepTextFlat Cell (3-D Rotation Properties Section)

Указывает, будет ли текст фигуры игнорировать поворот фигуры в 3-D. Не применяется к 2-D повороту. 
  
****

|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Текст фигуры не поворачивается вместе с геометрией фигуры.  <br/> |
|FALSE  <br/> |Текст фигуры преобразуется для поворота с геометрией фигуры.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **KeepTextFlat** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |KeepTextFlat  <br/> |
   
Чтобы получить ссылку на ячейку **KeepTextFlat** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRow3DRotationProperties** <br/> |
|Индекс ячейки:  <br/> |**visKeepTextFlat** <br/> |
   

