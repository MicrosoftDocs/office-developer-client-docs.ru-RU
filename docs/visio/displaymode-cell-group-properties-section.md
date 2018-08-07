---
title: Ячейка DisplayMode (раздел "Свойства группы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251623
localization_priority: Normal
ms.assetid: e6d72529-aa03-e94b-130c-79ed04336299
description: Определяет способ отображения групповой фигуры и ее компонентов.
ms.openlocfilehash: 086685b47d8eaf170a8722f7cd00545230541e79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813608"
---
# <a name="displaymode-cell-group-properties-section"></a>Ячейка DisplayMode (раздел "Свойства группы")

Определяет способ отображения групповой фигуры и ее компонентов.
  
|**Значение**|**Режим отображения**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Скрывает групповой фигуры и текст.  <br/> |**visGrpDispModeNone** <br/> |
|1  <br/> |Отображает групповой фигуры за фигурами.  <br/> |**visGrpDispModeBack** <br/> |
|2  <br/> |Отображает групповой фигуры перед фигурами.  <br/> |**visGrpDispModeFront** <br/> |
   
## <a name="remarks"></a>Замечания

Также задается это значение выбора группы, щелкнув **поведение** группы **Разработки фигуры** на вкладки " [Разработчик](run-in-developer-mode-display-the-developer-tab.md) ", а затем выбрав режим отображения в списке **группы данных** . 
  
Для получения ссылки на ячейки DisplayMode по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |DisplayMode  <br/> |
   
Для получения ссылки на ячейки DisplayMode по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowGroup** <br/> |
|Индекс ячейки:  <br/> |**visGroupDisplayMode** <br/> |
   

