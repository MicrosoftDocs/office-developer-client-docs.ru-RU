---
title: FillGradientDir Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Определяет направление градиента заполнения. Градиент может быть линейным, радиальным, прямоугольным или следовать по пути.
ms.openlocfilehash: 53aad056c7fc1674e00e142fd72a10134103b390
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406719"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a>FillGradientDir Cell (Gradient Properties Section)

Определяет направление градиента заполнения. Градиент может быть линейным, радиальным, прямоугольным или следовать по пути. 
  
> [!NOTE]
> Линейный градиент — это единственный градиент, который принимает дополнительное значение угла (как определяется ячейкой **FillGradientDir).** Все остальные направления градиента имеют заранее. 
  
****

|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Линейный градиент. Ячейка **FillGradientAngle** определяет направление градиента.  <br/> |
|1-7  <br/> |Радиальные градиенты. Градиент простирается наружу по кругу из центральной точки.  <br/> |
|8-12  <br/> |Прямоугольные градиенты. Градиент расширяется в виде направления от начала с прямоугольной формой.  <br/> |
|13  <br/> |Градиент пути.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **FillGradientDir** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы с использованием свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | FillGradientDir  <br/> |
   
Чтобы получить ссылку на ячейку **FillGradientDir** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowGradientProperties** <br/> |
| Индекс ячейки:  <br/> |**visFillGradientDir** <br/> |
   

