---
title: LineGradientDir Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: Определяет направление градиента линии. Градиент может быть линейным, радиальным, прямоугольным или следовать по пути.
ms.openlocfilehash: 05dcc6904a4e67d97c632dba44635936b1c14049
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417989"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a>LineGradientDir Cell (Gradient Properties Section)

Определяет направление градиента линии. Градиент может быть линейным, радиальным, прямоугольным или следовать по пути. 
  
> [!NOTE]
> Линейный градиент — это единственный градиент, который принимает дополнительное значение угла (определяется ячейкой **LineGradientDir).** Все остальные направления градиента имеют предустановленные enumerations. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Линейный градиент. Ячейка **LineGradientAngle** определяет направление градиента.  <br/> |
|1-7  <br/> |Радиальные градиенты. Градиент расширяется по кругу от центральной точки.  <br/> |
|8-12  <br/> |Прямоугольные градиенты. Градиент расширяется как направленная линия от начала с прямоугольным исчезаемым цветом.  <br/> |
|13   <br/> |Градиент пути.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **LineGradientDir** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LineGradientDir  <br/> |
   
Чтобы получить ссылку на ячейку **LineGradientDir** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowGradientProperties** <br/> |
| Индекс ячейки:  <br/> |**visLineGradientDir** <br/> |
   

