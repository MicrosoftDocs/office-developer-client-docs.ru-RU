---
title: ShapePlowCode Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm900
localization_priority: Normal
ms.assetid: acf07fd7-6aa6-1a92-9b7a-bd6fea8a7cb2
description: Определяет, перемещается ли эта замежаемая фигура, когда вы передвигаете другую фигуру рядом с этой фигурой на странице рисования.
ms.openlocfilehash: 6e155103f7bfc70a78826297f441fc9ce78942ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423897"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a>ShapePlowCode Cell (Shape Layout Section)

Определяет, перемещается ли эта замежаемая фигура, когда вы передвигаете другую фигуру рядом с этой фигурой на странице рисования.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Plow as page specifies.  <br/> |**visSLOPlowDefault** <br/> |
|1   <br/> |Plow no shapes.  <br/> |**visSLOPlowNever** <br/> |
|2   <br/> |Plow every shape.  <br/> |**visSLOPlowAlways** <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить значение этой ячейки для определенной фигуры на вкладке "Размещение" [](run-in-developer-mode-display-the-developer-tab.md) в диалоговом  окне "Поведение" (с выбранной фигурой на вкладке "Разработчик" в группе "Конструктор фигур" щелкните "Поведение" и выберите вкладку **"Размещение").**   
  
Чтобы настроить это поведение для  *всех*  фигур на странице рисования, используйте ячейку PlowCode в разделе "Макет страницы". 
  
Чтобы получить ссылку на ячейку ShapePlowCode по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |ShapePlowCode  <br/> |
   
Чтобы получить ссылку на ячейку ShapePlowCode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
|Индекс ячейки:  <br/> |**visSLOPlowCode** <br/> |
   

