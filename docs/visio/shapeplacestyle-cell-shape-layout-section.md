---
title: Ячейка ShapePlaceStyle (раздел "Макет фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm70007
localization_priority: Normal
ms.assetid: 29bfe8ec-ca12-8fbf-b62b-ece3710dfe2e
description: Указывает размещение фигуры на странице расположения фигур в диалоговом окне "Настройка макета" (на вкладке конструктор в группе макет нажмите кнопку Изменить расположение и нажмите кнопку Дополнительные параметры расположения). Сохранение макета стиля и выравнивание значений из VisCellIndices.
ms.openlocfilehash: f160c09eae3a3135360f2b8bf6df86c78ba0968c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814781"
---
# <a name="shapeplacestyle-cell-shape-layout-section"></a>Ячейка ShapePlaceStyle (раздел "Макет фигуры")

Указывает размещение фигуры на странице расположения фигур в диалоговом окне " **Настройка макета** " (на вкладке **Конструктор** в группе **Макет** нажмите кнопку **Изменить расположение**и нажмите кнопку **Дополнительные параметры расположения**). Сохранение макета стиля и выравнивание значений из **VisCellIndices**. 
  
|**Constant**|**Значение**|
|:-----|:-----|
|**visLOPlaceBottomToTop** <br/> |4  <br/> |
|**visLOPlaceCircular** <br/> |6  <br/> |
|**visLOPlaceCompactDownLeft** <br/> |14  <br/> |
|**visLOPlaceCompactDownRight** <br/> |7  <br/> |
|**visLOPlaceCompactLeftDown** <br/> |13  <br/> |
|**visLOPlaceCompactLeftUp** <br/> |12  <br/> |
|**visLOPlaceCompactRightDown** <br/> |8  <br/> |
|**visLOPlaceCompactRightUp** <br/> |9  <br/> |
|**visLOPlaceCompactUpLeft** <br/> |11  <br/> |
|**visLOPlaceCompactUpRight** <br/> |10  <br/> |
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
|**visLOPlaceHierarchyTopToBottomCenter** <br/> |17  <br/> |
|**visLOPlaceHierarchyTopToBottomLeft** <br/> |16  <br/> |
|**visLOPlaceHierarchyTopToBottomRight** <br/> |18  <br/> |
|**visLOPlaceLeftToRight** <br/> |2  <br/> |
|**visLOPlaceParentDefault** <br/> |15  <br/> |
|**visLOPlaceRadial** <br/> |3  <br/> |
|**visLOPlaceRightToLeft** <br/> |5  <br/> |
|**visLOPlaceTopToBottom** <br/> |1  <br/> |
   
Для ссылки на ячейки ShapePlaceStyle по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |ShapePlaceStyle  <br/> |
   
Для ссылки на ячейки ShapePlaceStyle по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
|Индекс ячейки:  <br/> |**visSLOPlaceStyle** <br/> |
   

