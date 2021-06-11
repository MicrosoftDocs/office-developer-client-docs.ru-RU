---
title: RotationType Cell (3-D Rotation Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Определяет, следует ли фигура параллельной вращению, повороту перспективы или косой вращению в виде шестерки от 0 до 6.
ms.openlocfilehash: 676f8a15185242aacc1affb9f1bd200ff3df454d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422945"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a>RotationType Cell (3-D Rotation Properties Section)

Определяет, следует ли фигура параллельной вращению, повороту перспективы или косой вращению в виде шестерки от 0 до 6. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Фигура не имеет поворота.  <br/> |
|1  <br/> |Фигура имеет параллельное вращение.  <br/> |
|2  <br/> |Фигура имеет поворот перспективы.  <br/> |
|3  <br/> |Фигура имеет левый верхний косый поворот.  <br/> |
|4   <br/> |Фигура имеет верхний правый косый поворот.  <br/> |
|5   <br/> |Фигура имеет левый нижний косый поворот.  <br/> |
|6   <br/> |Фигура имеет поворот в правом нижнем низу.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **RotationType** по имени из другой формулы, по значению **атрибута N** элемента **Cell** или из программы с использованием свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |RotationType  <br/> |
   
Чтобы получить ссылку на ячейку **RotationType** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRow3DRotationProperties** <br/> |
|Индекс ячейки:  <br/> |**visRotationType** <br/> |
   

