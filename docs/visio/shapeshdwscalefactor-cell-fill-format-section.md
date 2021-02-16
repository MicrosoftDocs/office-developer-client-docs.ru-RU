---
title: ShapeShdwScaleFactor Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033175
localization_priority: Normal
ms.assetid: 94ec06c5-8d2f-dd27-1eed-1abaf93daba8
description: Указывает процент увеличения или уменьшения тени фигуры.
ms.openlocfilehash: 5862b61ca1f5df25ca97bf8742b9e20bf45091a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436267"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a>ShapeShdwScaleFactor Cell (Fill Format Section)

Указывает процент увеличения или уменьшения тени фигуры.
  
## <a name="remarks"></a>Примечания

Каждая тень имеет затеняемое расположение закрепления, которое является точкой на тени, соответствующей контакту фигуры. Например, если контакт фигуры находится в центре фигуры, то расположение закрепления в тени будет точкой в центре тени. При применении масштабирования к простым тени увеличение по центру расположено на затененом контакте; При применении масштабирования к косой тени увеличение применяется в направлении косой границы. 
  
Чтобы установить это значение для всех фигур на странице, используйте ячейку ShdwScaleFactor в разделе "Свойства страницы".
  
Это значение соответствует значению  параметра увеличения в диалоговом окне "Тени" (на вкладке "Главная" в группе фигур щелкните "Тени" и выберите **"Параметры тени").**   
  
Чтобы получить ссылку на ячейку ShapeShdwScaleFactor по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |ShapeShdwScaleFactor  <br/> |
   
Чтобы получить ссылку на ячейку ShapeShdwScaleFactor по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowFill** <br/> |
|Индекс ячейки:  <br/> |**visFillShdwScaleFactor** <br/> |
   

