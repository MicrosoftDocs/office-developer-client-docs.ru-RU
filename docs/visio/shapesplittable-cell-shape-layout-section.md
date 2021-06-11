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
description: Указывает, можно ли разделить эту 1-D-форму.
ms.openlocfilehash: 9f92cf7d147be8e59d860bcc8a958bf0cdc008c6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427075"
---
# <a name="shapesplittable-cell-shape-layout-section"></a>ShapeSplittable Cell (Shape Layout Section)

Указывает, можно ли разделить эту 1-D-форму. 
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Не допускайте разделения этой фигуры.  <br/> |**visSLOSplittableNone** <br/> |
| 1  <br/> | Разрешить разделение этой фигуры.  <br/> |**visSLOSplittableAllow** <br/> |
   
## <a name="remarks"></a>Примечания

Поведение соединители и другие 1-D формы по умолчанию зависит от типа рисования. 
  
Автоматическое разделение фигур включено и отключено на трех различных уровнях: приложения, страницы и формы. По умолчанию разделение включено на уровне приложений и уровнях страниц. 
  
Чтобы включить или отключить разделение на уровне  приложения, воспользуйтесь параметром разделения соединители Enable на вкладке **Advanced** диалогового окна **Visio Options** (щелкните вкладку **Файл,** щелкните Параметры **и** нажмите кнопку **Advanced).** 
  
Чтобы включить или отключить разделение на странице, см. [ячейку PageShapeSplit.](pageshapesplit-cell-page-layout-section.md) 
  
Чтобы форма смогла разделить 1-D разделимые фигуры, см. в [разделе ShapeSplit](shapesplit-cell-shape-layout-section.md) cell. 
  
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
   

