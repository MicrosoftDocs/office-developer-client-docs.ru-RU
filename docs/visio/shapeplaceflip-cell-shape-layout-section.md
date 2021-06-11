---
title: ShapePlaceFlip Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253247
localization_priority: Normal
ms.assetid: 40008507-d9e4-9c0e-603f-d5e6da73a94b
description: Определяет, как фигура переворачивается, вращается или как на странице, когда вы закладываете фигуры, используя диалоговое окно Configure Layout (на вкладке Дизайн, в группе Макет, щелкните Re-Layout Страницу, а затем нажмите кнопку Дополнительные параметры макета).
ms.openlocfilehash: 72ef1b67dd87d842e6a4372d1eb08d614f0eb2d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429280"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a>ShapePlaceFlip Cell (Shape Layout Section)

Определяет, как фигура переворачивается, вращается или как на странице, когда вы закладываете фигуры, используя  диалоговое окно **Configure** **Layout**(на вкладке Design, в группе **Макет,** щелкните страницу повторного макета **и** нажмите кнопку Дополнительные параметры макета).
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Использование по умолчанию страницы.  <br/> |**visLOFlipDefault** <br/> |
|1  <br/> |Переверните горизонтально.  <br/> |**visLOFlipX** <br/> |
|2  <br/> |Переверните вертикаль.  <br/> |**visLOFlipY** <br/> |
|4   <br/> |Переверните 90-градусные приращения между 0 и 270.  <br/> |**visLOFlipRotate** <br/> |
|8   <br/> |Не переворачивать.  <br/> |**visLOFlipNone** <br/> |
   
## <a name="remarks"></a>Примечания

Значение в ячейке ShapePlaceFlip помогает сориентировать фигуру на следующую, к ней подключенную.
  
Чтобы установить это поведение для  *всех*  фигур на странице рисования, используйте ячейку PlaceFlip в разделе Макет страницы. 
  
Чтобы получить ссылку на ячейку ShapePlaceFlip по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |ShapePlaceFlip  <br/> |
   
Чтобы получить ссылку на ячейку ShapePlaceFlip по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
|Индекс ячейки:  <br/> |**visSLOPlaceFlip** <br/> |
   

