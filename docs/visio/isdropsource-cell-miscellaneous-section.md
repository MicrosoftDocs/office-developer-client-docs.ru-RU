---
title: Ячейка IsDropSource (раздел "Прочее")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm490
localization_priority: Normal
ms.assetid: 3b20e6ef-f1ac-5bb0-5ac3-4df3ae5e9bf9
description: Определяет, будет ли фигуры можно добавить в группу, перетащите его в группу.
ms.openlocfilehash: f2edfcb7cf9d21b2ecd97b335b07f30233903d5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813978"
---
# <a name="isdropsource-cell-miscellaneous-section"></a>Ячейка IsDropSource (раздел "Прочее")

Определяет, будет ли фигуры можно добавить в группу, перетащите его в группу.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Можно добавить фигуру в группу, перетащите его в группу.  <br/> |
|FALSE  <br/> |Не удается добавить фигуру в группу.  <br/> |
   
## <a name="remarks"></a>Замечания

Также можно задать это значение, выбрав фигуры, щелкая вкладки " [Разработчик](run-in-developer-mode-display-the-developer-tab.md) " **поведение** и затем установите флажок **Добавить фигуру в группы при размещении** . 
  
Дополнение к разрешению это поведение для фигуры, необходимо также включить группу, чтобы принять фигур, перетащенных в нее. Для этого выберите группу, щелкните **поведение** на вкладке [Разработчик](run-in-developer-mode-display-the-developer-tab.md) и установите флажок **Accept добавленной фигур** . Это значение хранится в ячейке IsDropTarget в разделе Свойства группы. 
  
Чтобы получить ссылку на ячейку IsDropSource по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |IsDropSource  <br/> |
   
Для получения ссылки на ячейки IsDropSource по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowMisc** <br/> |
|Индекс ячейки:  <br/> |**visDropSource** <br/> |
   

