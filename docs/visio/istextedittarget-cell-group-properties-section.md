---
title: Ячейка IsTextEditTarget (раздел "Свойства группы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251627
localization_priority: Normal
ms.assetid: 355cef8b-9213-479a-af95-b591f4bc51ad
description: Определяет назначение текста для группы.
ms.openlocfilehash: 65baf90254f6b213efea04739d8e4a66952b2856
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814016"
---
# <a name="istextedittarget-cell-group-properties-section"></a>Ячейка IsTextEditTarget (раздел "Свойства группы")

Определяет назначение текста для группы.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Текст добавляется в группы фигур.  <br/> |
|FALSE  <br/> |Текст добавляется фигура в группе в верхней части порядок размещения.  <br/> |
   
## <a name="remarks"></a>Замечания

Также можно задать это значение, выбрав в группу, щелкая вкладки " [Разработчик](run-in-developer-mode-display-the-developer-tab.md) " **поведение** и затем установите флажок **Изменить текст группы** . 
  
Группы, созданные в версиях, более ранних чем Visio 2000 имеют значение по умолчанию FALSE. Приступая к работе с Visio версии 2000, значение по умолчанию — TRUE. 
  
Чтобы получить ссылку на ячейку IsTextEditTarget по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |IsTextEditTarget  <br/> |
   
Для получения ссылки на ячейки IsTextEditTarget по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowGroup** <br/> |
|Индекс ячейки:  <br/> |**visGroupIsTextEditTarget** <br/> |
   

