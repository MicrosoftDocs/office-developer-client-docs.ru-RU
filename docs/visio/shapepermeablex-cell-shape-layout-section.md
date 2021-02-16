---
title: ShapePermeableX Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm890
localization_priority: Normal
ms.assetid: 7e27b36c-4fd1-34e0-c168-f49eb5757b0e
description: Определяет, может ли соединителю маршрут следования по горизонтали проходить через заметоряемую фигуру.
ms.openlocfilehash: 21fa1683c4b1afd24992ec7a8a6daa52a8280825
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409477"
---
# <a name="shapepermeablex-cell-shape-layout-section"></a>ShapePermeableX Cell (Shape Layout Section)

Определяет, может ли соединителю маршрут следования по горизонтали проходить через заметоряемую фигуру.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Позволяет соединителю перенаровняться по горизонтали через заметоряемую фигуру.  <br/> |
|FALSE  <br/> |Не разрешайте соединителю маршрут по горизонтали через заметоряемую фигуру.  <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить значение этой  ячейки  на вкладке "Размещение" в диалоговом окне  "Поведение" (с выбранной фигурой, на вкладке "Разработчик", в группе "Проектирование фигуры" щелкните "Поведение" и выберите вкладку **"Размещение").** [](run-in-developer-mode-display-the-developer-tab.md) 
  
В версиях, более ранних, чем Visio 2000, такое поведение задано с помощью ячейки ObjInteract в разделе "Прочие". 
  
Чтобы получить ссылку на ячейку ShapePermeableX по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |ShapePermeableX  <br/> |
   
Чтобы получить ссылку на ячейку ShapePermeableX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
|Индекс ячейки:  <br/> |**visSLOPermX** <br/> |
   

