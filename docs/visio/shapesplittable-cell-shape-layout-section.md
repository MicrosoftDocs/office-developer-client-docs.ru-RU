---
title: ShapeSplittable Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60081
localization_priority: Normal
ms.assetid: 6330304a-71f3-62b4-1b27-14495e3f12c3
description: Указывает, можно ли разделить эту 1-D-фигуру.
ms.openlocfilehash: 9f92cf7d147be8e59d860bcc8a958bf0cdc008c6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427075"
---
# <a name="shapesplittable-cell-shape-layout-section"></a>ShapeSplittable Cell (Shape Layout Section)

Указывает, можно ли разделить эту 1-D-фигуру. 
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Не разрешите разделять эту фигуру.  <br/> |**visSLOSplittableNone** <br/> |
| 1   <br/> | Разрешить разделение фигуры.  <br/> |**visSLOSplittableAllow** <br/> |
   
## <a name="remarks"></a>Примечания

Поведение по умолчанию для соединители и других 1-D фигур зависит от типа рисования. 
  
Автоматическое разделение фигур включено и отключено на трех разных уровнях: приложения, страницы и фигуры. По умолчанию разделение включено на уровне приложения и страницы. 
  
Чтобы включить или отключить разделение на уровне приложения, используйте параметр разделения  соединители enable на вкладке "Дополнительные  параметры" диалогового окна "Параметры **Visio"** (щелкните вкладку "Файл", выберите "Параметры" и нажмите кнопку  "Дополнительные").  
  
Чтобы включить или отключить разделение на странице, см. [ячейку PageShapeSplit.](pageshapesplit-cell-page-layout-section.md) 
  
Чтобы фигура смогла разделить разделенные фигуры, см. в [ячейке ShapeSplit.](shapesplit-cell-shape-layout-section.md) 
  
Чтобы получить ссылку на ячейку ShapeSplittable по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | ShapeSplittable  <br/> |
   
Чтобы получить ссылку на ячейку ShapeSplittable по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
| Индекс ячейки:  <br/> |**visSLOSplittable** <br/> |
   

