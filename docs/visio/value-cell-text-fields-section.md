---
title: Value Cell (Text Fields Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1095
localization_priority: Normal
ms.assetid: 3ca662c8-1ce4-89a9-3264-1ba533fcd444
description: Содержит функцию для поля.
ms.openlocfilehash: d5a09dd0d59341125db897484f74addff22328de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430947"
---
# <a name="value-cell-text-fields-section"></a>Value Cell (Text Fields Section)

Содержит функцию для поля.
  
## <a name="remarks"></a>Примечания

Значение этой ячейки можно задать с помощью диалогового окна " **поле** " (на вкладке **Вставка** в группе **текст** выберите **поле**).
  
Чтобы получить ссылку на ячейку значения по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Fields. Value [ *i* ], где *i* = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку value по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**Виссектионтекстфиелд** <br/> |
|Индекс строки:  <br/> |**висровфиелд** +  *i* , где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**Висфиелдцелл** <br/> |
   

