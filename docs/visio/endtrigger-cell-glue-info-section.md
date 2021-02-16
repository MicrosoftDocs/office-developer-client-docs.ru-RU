---
title: EndTrigger Cell (Glue Info Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251331
localization_priority: Normal
ms.assetid: 8dc6515b-66ab-f1ac-18fd-820209f90991
description: Содержит формулу триггера, сгенерированную приложением, которая определяет, следует ли перемещать конечную точку однообразной фигуры для поддержания подключения к другой фигуре.
ms.openlocfilehash: 9093cca782d9262b2511198ed73f512a75bb8994
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418584"
---
# <a name="endtrigger-cell-glue-info-section"></a>EndTrigger Cell (Glue Info Section)

Содержит формулу триггера, сгенерированную приложением, которая определяет, следует ли перемещать конечную точку однообразной фигуры для поддержания подключения к другой фигуре.
  
## <a name="remarks"></a>Примечания

При привязывке одномерной фигуры к другой фигуре с помощью динамического приклейки Visio создает формулу, которая ссылается на ячейку EventXFMod другой фигуры. При смене этой фигуры Visio пересчитает все формулы, которые ссылаются на ее ячейку EventXFMod, включая формулу в ячейке EndTrigger. Другие формулы 1-D фигуры ссылаются на ячейку EndTrigger и перемещают конечную точку 1-D фигуры или изменяют ее по мере необходимости.
  
Чтобы получить ссылку на ячейку EndTrigger по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | EndTrigger  <br/> |
   
Чтобы получить ссылку на ячейку EndTrigger по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowMisc** <br/> |
| Индекс ячейки:  <br/> |**visEndTrigger** <br/> |
   

