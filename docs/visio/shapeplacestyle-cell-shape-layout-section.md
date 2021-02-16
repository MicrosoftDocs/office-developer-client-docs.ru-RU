---
title: ShapePlaceStyle Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm70007
localization_priority: Normal
ms.assetid: 29bfe8ec-ca12-8fbf-b62b-ece3710dfe2e
description: Указывает, как фигуры помещаются на страницу, когда фигуры размещаются в диалоговом окне "Настройка макета" (на вкладке "Конструктор" в группе "Макет" щелкните Re-Layout "Страница" и выберите "Дополнительные параметры макета"). Хранит значения стиля макета и выравнивания из VisCellIndices.
ms.openlocfilehash: 381f74912b64395f33a2dc55c0bad24d36a16286
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418577"
---
# <a name="shapeplacestyle-cell-shape-layout-section"></a>ShapePlaceStyle Cell (Shape Layout Section)

Указывает, как фигуры помещаются на страницу  при размещении фигур в  диалоговом  окне "Настройка макета" (на вкладке "Конструктор" в группе "Макет" щелкните "Страница повторного макета" **и** выберите "Дополнительные параметры макета").  Хранит значения стиля макета и выравнивания **из VisCellIndices.** 
  
|**Константа**|**Значение**|
|:-----|:-----|
|**visLOPlaceBottomToTop** <br/> |4   <br/> |
|**visLOPlaceCircular** <br/> |6   <br/> |
|**visLOPlaceCompactDownLeft** <br/> |14   <br/> |
|**visLOPlaceCompactDownRight** <br/> |7   <br/> |
|**visLOPlaceCompactLeftDown** <br/> |13   <br/> |
|**visLOPlaceCompactLeftUp** <br/> |12   <br/> |
|**visLOPlaceCompactRightDown** <br/> |8   <br/> |
|**visLOPlaceCompactRightUp** <br/> |9   <br/> |
|**visLOPlaceCompactUpLeft** <br/> |11  <br/> |
|**visLOPlaceCompactUpRight** <br/> |10   <br/> |
|**visLOPlaceDefault** <br/> |0  <br/> |
|**visLOPlaceHierarchyBottomToTopCenter** <br/> |20  <br/> |
|**visLOPlaceHierarchyBottomToTopLeft** <br/> |19  <br/> |
|**visLOPlaceHierarchyBottomToTopRight** <br/> |21  <br/> |
|**visLOPlaceHierarchyLeftToRightBottom** <br/> |24  <br/> |
|**visLOPlaceHierarchyLeftToRightMiddle** <br/> |23  <br/> |
|**visLOPlaceHierarchyLeftToRightTop** <br/> |22  <br/> |
|**visLOPlaceHierarchyRightToLeftBottom** <br/> |27  <br/> |
|**visLOPlaceHierarchyRightToLeftMiddle** <br/> |26  <br/> |
|**visLOPlaceHierarchyRightToLeftTop** <br/> |25  <br/> |
|**visLOPlaceHierarchyTopToBottomCenter** <br/> |17   <br/> |
|**visLOPlaceHierarchyTopToBottomLeft** <br/> |16   <br/> |
|**visLOPlaceHierarchyTopToBottomRight** <br/> |18   <br/> |
|**visLOPlaceLeftToRight** <br/> |2   <br/> |
|**visLOPlaceParentDefault** <br/> |15   <br/> |
|**visLOPlaceRadial** <br/> |3   <br/> |
|**visLOPlaceRightToLeft** <br/> |5   <br/> |
|**visLOPlaceTopToBottom** <br/> |1   <br/> |
   
Чтобы сослаться на ячейку ShapePlaceStyle по имени из другой формулы или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |ShapePlaceStyle  <br/> |
   
Чтобы сослаться на ячейку ShapePlaceStyle по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
|Индекс ячейки:  <br/> |**visSLOPlaceStyle** <br/> |
   

