---
title: PageShapeSplit Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033777
localization_priority: Normal
ms.assetid: 4d3bdf77-0ad4-86a4-d215-1d5a5fbe33f7
description: Указывает, можно ли автоматически разделить фигуры на странице.
ms.openlocfilehash: 18a40e0876b117556a1e7ab43f640e798dc248c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422021"
---
# <a name="pageshapesplit-cell-page-layout-section"></a>PageShapeSplit Cell (Page Layout Section)

Указывает, можно ли автоматически разделить фигуры на странице.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Не допускайте автоматического разделения фигуры.  <br/> |**visPLOSplitNone** <br/> |
|1  <br/> |Разрешить автоматическое разделение фигуры (по умолчанию).  <br/> |**visPLOSplitAllow** <br/> |
   
## <a name="remarks"></a>Примечания

Автоматическое разделение фигур включено и отключено на трех различных уровнях: приложения, страницы и формы. По умолчанию разделение включено на уровнях приложений и страниц. Параметр по умолчанию для фигур зависит от типа рисования. 
  
Чтобы включить или отключить разделение на уровне  приложения, воспользуйтесь параметром разделения соединители Enable на вкладке **Advanced** диалогового окна Visio  **Options** (щелкните кнопку **Office,** нажмите кнопку Параметры на вкладке **Visio** и нажмите **кнопку Advanced).** 
  
Чтобы включить или отключить разделение на уровне фигуры, см. в разделе ShapeSplit и ShapeSplittable cells. 
  
Чтобы получить ссылку на ячейку PageShapeSplit по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |PageShapeSplit  <br/> |
   
Чтобы получить ссылку на ячейку PageShapeSplit по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPageLayout** <br/> |
|Индекс ячейки:  <br/> |**visPLOSplit** <br/> |
   

