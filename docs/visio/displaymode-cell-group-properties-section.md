---
title: DisplayMode Cell (Group Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251623
localization_priority: Normal
ms.assetid: e6d72529-aa03-e94b-130c-79ed04336299
description: Определяет способ отображения фигуры группы и ее членов.
ms.openlocfilehash: a49d7a38eac75a2845de0ca3ad22f7cbf79a63df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332713"
---
# <a name="displaymode-cell-group-properties-section"></a>DisplayMode Cell (Group Properties Section)

Определяет способ отображения фигуры группы и ее членов.
  
|**Значение**|**Режим отображения**|**Константа автоматизации**|
|:-----|:-----|:-----|
|нуль  <br/> |Скрывает фигуру группы и текст.  <br/> |**Висгрпдиспмоденоне** <br/> |
|1,1  <br/> |Отображает фигуру группы позади фигур элементов.  <br/> |**Висгрпдиспмодебакк** <br/> |
|2  <br/> |Отображает фигуру группы перед фигурами элементов.  <br/> |**Висгрпдиспмодефронт** <br/> |
   
## <a name="remarks"></a>Комментарии

Это значение можно также задать, выбрав группу, щелкнув **поведение** в группе **Макет фигуры** на вкладке [разработчик](run-in-developer-mode-display-the-developer-tab.md) , а затем выбрав режим отображения в списке **данные группы** . 
  
Чтобы получить ссылку на ячейку DisplayMode по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |DisplayMode  <br/> |
   
Чтобы получить ссылку на ячейку DisplayMode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**Висровграуп** <br/> |
|Индекс ячейки:  <br/> |**Висграупдисплаймоде** <br/> |
   

