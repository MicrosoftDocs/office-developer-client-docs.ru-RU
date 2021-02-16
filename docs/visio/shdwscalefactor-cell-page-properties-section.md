---
title: ShdwScaleFactor Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60083
localization_priority: Normal
ms.assetid: 10979706-6dfe-5241-e862-3f94716d14fa
description: Указывает процент для увеличения или уменьшения тени фигуры.
ms.openlocfilehash: 9175e9a1148779524fdce96ff18eac22fe8dd421
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429007"
---
# <a name="shdwscalefactor-cell-page-properties-section"></a>ShdwScaleFactor Cell (Page Properties Section)

Указывает процент для увеличения или уменьшения тени фигуры. 
  
## <a name="remarks"></a>Примечания

Каждая тень имеет затеняемое расположение закрепления, которое является точкой на тени, соответствующей контакту фигуры. Например, если контакт фигуры находится в центре фигуры, то расположение закрепления в тени будет точкой в центре тени. При применении масштабирования к простым тени увеличение по центру расположено на затененом контакте; При применении масштабирования к косой тени увеличение применяется в направлении косой границы. 
  
 Этот процент используется, когда для типа теней для фигуры установлено значение Page Default (ячейка ShapeShdwType равна ** visFSTPageDefault ** ). 
  
Чтобы настроить это поведение для отдельной фигуры, используйте ячейку ShapeShdwScaleFactor в разделе "Формат заливки".
  
Это значение соответствует значению  в окне увеличения на  вкладке "Тени" в диалоговом окне "Настройка страницы" (на вкладке "Конструктор" щелкните стрелку **"Настройка** страницы").   
  
Чтобы получить ссылку на ячейку ShdwScaleFactor по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | ShdwScaleFactor  <br/> |
   
Чтобы получить ссылку на ячейку ShdwScaleFactor по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPage** <br/> |
| Индекс ячейки:  <br/> |**visPageShdwScaleFactor** <br/> |
   

