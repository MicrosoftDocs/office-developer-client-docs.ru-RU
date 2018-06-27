---
title: Ячейка PageShapeSplit (раздел макет страницы)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033777
localization_priority: Normal
ms.assetid: 4d3bdf77-0ad4-86a4-d215-1d5a5fbe33f7
description: Указывает, может ли автоматически разделение фигур на странице.
ms.openlocfilehash: 7f1df0158cde6853c5518597c853cb56151eefbc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814353"
---
# <a name="pageshapesplit-cell-page-layout-section"></a>Ячейка PageShapeSplit (раздел макет страницы)

Указывает, может ли автоматически разделение фигур на странице.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Не разрешать разделение автоматического фигуры.  <br/> |**visPLOSplitNone** <br/> |
|1  <br/> |Разрешить автоматическое фигуры разделение (по умолчанию).  <br/> |**visPLOSplitAllow** <br/> |
   
## <a name="remarks"></a>Замечания

Автоматическое разделение фигур включена и отключена три уровня: приложения, страницы и фигуры. По умолчанию разделение включена на уровне приложения и страницы. Значение по умолчанию для фигур зависит от типа документа. 
  
Чтобы включить или отключить разделение на уровне приложения, используйте параметр **включить разделение соединительной линии** на вкладке **Дополнительно** диалогового окна **Параметры Visio** (нажмите кнопку **Office** , выберите команду **Параметры** в **Visio** а затем щелкните **Дополнительно** ). 
  
Чтобы включить или отключить разделение на уровне фигур, обратитесь к разделу ячейки ShapeSplit и ShapeSplittable. 
  
Чтобы получить ссылку на ячейку PageShapeSplit по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |PageShapeSplit  <br/> |
   
Для получения ссылки на ячейки PageShapeSplit по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPageLayout** <br/> |
|Индекс ячейки:  <br/> |**visPLOSplit** <br/> |
   
