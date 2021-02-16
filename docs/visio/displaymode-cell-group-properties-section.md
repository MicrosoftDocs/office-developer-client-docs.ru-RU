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
description: Определяет, как отображается фигура группы и ее члены.
ms.openlocfilehash: a49d7a38eac75a2845de0ca3ad22f7cbf79a63df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413187"
---
# <a name="displaymode-cell-group-properties-section"></a>DisplayMode Cell (Group Properties Section)

Определяет, как отображается фигура группы и ее члены.
  
|**Значение**|**Режим отображения**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Скрывает фигуру и текст группы.  <br/> |**visGrpDispModeNone** <br/> |
|1   <br/> |Отображает фигуру группы за фигурами членов.  <br/> |**visGrpDispModeBack** <br/> |
|2   <br/> |Отображает фигуру группы перед фигурами членов.  <br/> |**visGrpDispModeFront** <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить это значение, выбрав  группу, щелкнув [](run-in-developer-mode-display-the-developer-tab.md) "Поведение" в группе "Проектирование фигур" на вкладке "Разработчик", а затем выбрав режим отображения в списке данных **группы.**  
  
Чтобы получить ссылку на ячейку DisplayMode по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |DisplayMode  <br/> |
   
Чтобы получить ссылку на ячейку DisplayMode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowGroup** <br/> |
|Индекс ячейки:  <br/> |**visGroupDisplayMode** <br/> |
   

