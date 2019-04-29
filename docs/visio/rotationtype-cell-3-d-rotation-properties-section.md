---
title: RotationType Cell (3-D Rotation Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Определяет, соответствует ли фигура параллельному повороту, повороту перспективы или наклонному повороту в виде целого числа от 0 до 6.
ms.openlocfilehash: 676f8a15185242aacc1affb9f1bd200ff3df454d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422945"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a>RotationType Cell (3-D Rotation Properties Section)

Определяет, соответствует ли фигура параллельному повороту, повороту перспективы или наклонному повороту в виде целого числа от 0 до 6. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|нуль  <br/> |Фигура не имеет вращения.  <br/> |
|1,1  <br/> |Фигура имеет параллельный поворот.  <br/> |
|2  <br/> |Фигура имеет перспективный поворот.  <br/> |
|4  <br/> |Фигура имеет верхний левый наклонный поворот.  <br/> |
|SP4  <br/> |Фигура имеет верхний правый наклонный угол.  <br/> |
|17:00  <br/> |Фигура имеет нижний поворот с наклоном влево.  <br/> |
|ICMPv6  <br/> |Фигура имеет нижний правый наклонный угол.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **RotationType** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |RotationType  <br/> |
   
Чтобы получить ссылку на ячейку **RotationType** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRow3DRotationProperties** <br/> |
|Индекс ячейки:  <br/> |**Висротатионтипе** <br/> |
   

