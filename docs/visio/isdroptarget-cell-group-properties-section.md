---
title: Ячейка IsDropTarget (раздел "Свойства группы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm495
localization_priority: Normal
ms.assetid: 8140fc7b-b99c-54bb-7af3-7de6fcdae7d3
description: Определяет, позволяет ли группы для добавления фигуры, перетащите его в группе.
ms.openlocfilehash: 326ead15bcdc72797853daee797d8f08d459a638
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813988"
---
# <a name="isdroptarget-cell-group-properties-section"></a>Ячейка IsDropTarget (раздел "Свойства группы")

Определяет, позволяет ли группы для добавления фигуры, перетащите его в группе.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Можно добавить фигуру в группу, перетащите его в группу.  <br/> |
|FALSE  <br/> |Не удалось удалить фигуру на группы.  <br/> |
   
## <a name="remarks"></a>Замечания

Также можно задать это значение, выбрав в группу, щелкая вкладки " [Разработчик](run-in-developer-mode-display-the-developer-tab.md) " **поведение** и затем выбрав флажок **Accept пропущенные фигур** . 
  
Чтобы добавить фигуру в группу, перетащите его в группе, необходимо также включить схожи фигуры. Выделите фигуру, выберите **поведение** на вкладке [Разработчик](run-in-developer-mode-display-the-developer-tab.md) и затем установите флажок **Добавить фигуру в группы при размещении** . Это значение хранится в ячейке IsDropSource в разделе Разное. 
  
Чтобы получить ссылку на ячейку IsDropTarget по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |IsDropTarget  <br/> |
   
Для получения ссылки на ячейки IsDropTarget по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowGroup** <br/> |
|Индекс ячейки:  <br/> |**visGroupIsDropTarget** <br/> |
   

