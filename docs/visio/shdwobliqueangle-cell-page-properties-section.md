---
title: ShdwObliqueAngle Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033178
localization_priority: Normal
ms.assetid: 2e0b9754-3e3b-3a26-4e1a-e09102055c20
description: Содержит число, определяющее угол наклона при применении типа тени страницы по умолчанию.
ms.openlocfilehash: 2eca29bbc735c7101ca82a2f26db30b2e344b8e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430429"
---
# <a name="shdwobliqueangle-cell-page-properties-section"></a>ShdwObliqueAngle Cell (Page Properties Section)

Содержит число, определяющее угол наклона при применении типа тени страницы по умолчанию.
  
## <a name="remarks"></a>Примечания

Значение ноль (0) в этой ячейке указывает на то, что направление угла является прямолинейным и измеряется при перемещении по часовой стрелке.
  
 Угол, описанный в этой ячейке, используется всякий раз, когда ячейка ShapeShdwType (тип тени для фигуры на странице) имеет значение Default страницы (**висфстпажедефаулт** ), а тип тени — наклонный. Тип тени страницы по умолчанию определяется в ячейке ShdwType. 
  
Чтобы задать такое поведение для отдельной фигуры, используйте ячейку ShapeShdwObliqueAngle в разделе Формат заливки.
  
Чтобы получить ссылку на ячейку ShdwObliqueAngle по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | ShdwObliqueAngle  <br/> |
   
Чтобы получить ссылку на ячейку ShdwObliqueAngle по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровпаже** <br/> |
| Индекс ячейки:  <br/> |**Виспажешдвобликуеангле** <br/> |
   

