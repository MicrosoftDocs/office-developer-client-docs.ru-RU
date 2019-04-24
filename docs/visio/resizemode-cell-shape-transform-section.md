---
title: ResizeMode Cell (Shape Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251203
localization_priority: Normal
ms.assetid: 49816e46-fa83-3ee4-1451-9c85fbd0f519
description: Показывает текущий параметр поведения изменения размера для фигуры.
ms.openlocfilehash: 7e9080fcd4604e2dbdc1dae31992f05e5b512213
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326882"
---
# <a name="resizemode-cell-shape-transform-section"></a>ResizeMode Cell (Shape Transform Section)

Показывает текущий параметр поведения изменения размера для фигуры.
  
|**Value**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|нуль  <br/> |Используйте параметр группы.  <br/> |**Висксформресизедонткаре** <br/> |
|1,1  <br/> |Только перестановка.  <br/> |**Висксформресизеспреад** <br/> |
|2  <br/> |Масштабирование с помощью Group.  <br/> |**Висксформресизескале** <br/> |
   
## <a name="remarks"></a>Замечания

Вы также можете задать это значение на вкладке **поведение** в диалоговом окне **поведение** (на вкладке [разработчик](run-in-developer-mode-display-the-developer-tab.md)в группе **Макет фигуры** щелкните **поведение**). Чтобы получить ссылку на ячейку ResizeMode по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |ResizeMode  <br/> |
   
Чтобы получить ссылку на ячейку ResizeMode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**Висровксформаут** <br/> |
|Индекс ячейки:  <br/> |**Висксформресиземоде** <br/> |
   

