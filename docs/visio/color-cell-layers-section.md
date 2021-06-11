---
title: Color Cell (Layers Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm165
localization_priority: Normal
ms.assetid: 61c19342-46fb-48d4-6375-c9ea8306286d
description: Указывает цвет, используемый для отображения слоя.
ms.openlocfilehash: a2eef24187165cabfdfc8dee49747a2381562d3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435133"
---
# <a name="color-cell-layers-section"></a>Color Cell (Layers Section)

Указывает цвет, используемый для отображения слоя.
  
## <a name="remarks"></a>Примечания

Чтобы установить цвет, введите число от 0 до 23.
  
Это значение ячейки соответствует параметру **цвета Layer** в диалоговом  окне **Свойства** слоя  (в группе редактирования на вкладке **Home** щелкните Слои и нажмите кнопку **Свойства слоя).**
  
Чтобы ввести настраиваемый цвет, используйте функцию RGB или HSL. Значение настраиваемого цвета — это цвет RGB, и RGB *(r, g, b),* а не номер будет показан в окне ShapeSheet. Пользовательские цвета, используемые в числовом режиме, имеют значения 24 и выше. Значение 255 указывает, что слой не имеет цвета. 
  
Можно установить прозрачность цвета слоя в ячейке Transparency.
  
Чтобы получить ссылку на ячейку Color по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Layers.Color[i] где *i* = <1>, 2, 3, ...   <br/> |
   
Чтобы получить ссылку на ячейку Color по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionLayer** <br/> |
|Индекс строки:  <br/> |**visRowLayer**  +   *i,* *где i* = 0, 1, 2, ...  <br/> |
|Индекс ячейки:  <br/> |**visLayerColor** <br/> |
   

