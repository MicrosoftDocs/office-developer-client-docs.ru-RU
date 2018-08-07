---
title: Ячейка ShapePermeableX (раздел "Макет фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm890
localization_priority: Normal
ms.assetid: 7e27b36c-4fd1-34e0-c168-f49eb5757b0e
description: Определяет, будет ли соединитель могут направляться по горизонтали размещаемой фигуры.
ms.openlocfilehash: 1e0fe614b9401ea453b9c650ef9af3b4105b3805
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19814778"
---
# <a name="shapepermeablex-cell-shape-layout-section"></a>Ячейка ShapePermeableX (раздел "Макет фигуры")

Определяет, будет ли соединитель могут направляться по горизонтали размещаемой фигуры.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Включение соединителей для маршрутизации по горизонтали через размещаемую фигуру.  <br/> |
|FALSE  <br/> |Нельзя допускать маршрут соединители горизонтально через размещаемую фигуру.  <br/> |
   
## <a name="remarks"></a>Замечания

Значение ячейки также можно настроить на вкладке **Размещение** в диалоговом окне **поведение** (с фигуры, выбранные на вкладке [Разработчик](run-in-developer-mode-display-the-developer-tab.md) в группе **Создать фигуру** нажмите кнопку **поведение**и затем перейдите на вкладку **Размещение** ). 
  
В версии более ранней, чем Visio 2000 устанавливаются это поведение с помощью ObjInteract ячейки в разделе Разное. 
  
Чтобы получить ссылку на ячейку ShapePermeableX по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |ShapePermeableX  <br/> |
   
Для получения ссылки на ячейки ShapePermeableX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
|Индекс ячейки:  <br/> |**visSLOPermX** <br/> |
   

