---
title: LineColor Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm535
localization_priority: Normal
ms.assetid: d857b48b-9a3d-a1e1-5ad2-6816a492c8ab
description: Определяет цвет строки фигуры.
ms.openlocfilehash: d0b4ebee6d96bc67c9ca45e8a6194cb91ed6c7f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416939"
---
# <a name="linecolor-cell-line-format-section"></a>LineColor Cell (Line Format Section)

Определяет цвет строки фигуры.
  
## <a name="remarks"></a>Примечания

Чтобы установить цвет строки, введите число от 0 до 23, которое является индексом в коллекцию цветов строки. Вы можете просмотреть коллекцию цветов строки в  диалоговом окне **Line** (на вкладке Главная, в группе **Shape** нажмите кнопку **Line,** указать на **вес,** а затем нажмите кнопку **Дополнительные линии).** Можно также установить значение LineColor в диалоговом окне **Line.** 
  
Чтобы ввести настраиваемый цвет, используйте функцию RGB или HSL. Значение настраиваемого цвета — это цвет RGB, и RGB *(r, g, b),* а не номер будет показан в окне ShapeSheet. Пользовательские цвета, используемые в числовом режиме, имеют значения 24 и выше. 
  
Вы можете установить прозрачность цвета строки в ячейке LineColorTrans.
  
Чтобы получить ссылку на ячейку LineColor по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |LineColor  <br/> |
   
Чтобы получить ссылку на ячейку LineColor по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowLine** <br/> |
|Индекс ячейки:  <br/> |**visLineColor** <br/> |
   

