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
description: Указывает процент, с помощью которого тень фигуры может быть увеличена или уменьшена.
ms.openlocfilehash: 5862b61ca1f5df25ca97bf8742b9e20bf45091a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436267"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a>ShapeShdwScaleFactor Cell (Fill Format Section)

Указывает процент, с помощью которого тень фигуры может быть увеличена или уменьшена.
  
## <a name="remarks"></a>Примечания

Каждая тень имеет затеняемое расположение пина, которое является точкой на тени, соответствующей пин-коду фигуры. Например, если пин-код фигуры находится в центре фигуры, то затеняемое расположение пина будет точкой в центре тени. При применении масштабирования к простым теням увеличение расположено в затененом расположении пин-кода; При применении масштабирования к косой тени в косом направлении применяется увеличение. 
  
Чтобы установить это значение для всех фигур на странице, используйте ячейку ShdwScaleFactor в разделе Свойства страниц.
  
Это значение соответствует значению параметра **Magnification** в диалоговом окне **Shadow** (на вкладке **Главная** в группе **Shape** щелкните Тень **и** нажмите кнопку **Параметры тени).**
  
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
   

