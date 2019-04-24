---
title: KeepTextFlat Cell (3-D Rotation Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Указывает, будет ли текст фигуры игнорировать Поворот фигуры в трехмерном виде. Не применяется к повороту на 2 D.
ms.openlocfilehash: fc8cf2fac431645876c7f81ed9864cb6c2036169
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360440"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a>KeepTextFlat Cell (3-D Rotation Properties Section)

Указывает, будет ли текст фигуры игнорировать Поворот фигуры в трехмерном виде. Не применяется к повороту на 2 D. 
  
****

|**Value**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Текст фигуры не поворачивается вместе с геометрическим объектом фигуры.  <br/> |
|FALSE  <br/> |Текст фигуры преобразуется в поворот с помощью геометрии фигуры.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **KeepTextFlat** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |KeepTextFlat  <br/> |
   
Чтобы получить ссылку на ячейку **KeepTextFlat** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRow3DRotationProperties** <br/> |
|Индекс ячейки:  <br/> |**Вискиптекстфлат** <br/> |
   

