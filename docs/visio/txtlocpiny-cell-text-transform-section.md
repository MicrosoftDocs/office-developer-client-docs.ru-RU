---
title: TxtLocPinY Cell (Text Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251276
localization_priority: Normal
ms.assetid: 3f46cfcf-7eac-4a37-e782-39f4e7f8fc43
description: 'Определяет координату y центра вращения блока текста относительно начала блока текста. По умолчанию используется следующая формула:'
ms.openlocfilehash: 937c4e9928d32d55e8336d192b1ecc6140fd8381
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414062"
---
# <a name="txtlocpiny-cell-text-transform-section"></a>TxtLocPinY Cell (Text Transform Section)

Определяет координату *y* центра вращения блока текста относительно начала блока текста. По умолчанию используется следующая формула: 
  
= TxtHeight \* 0,5
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку TxtLocPinY по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | TxtLocPinY  <br/> |
   
Чтобы получить ссылку на ячейку TxtLocPinY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**висровтекстксформ** <br/> |
| Индекс ячейки:  <br/> |**висксформлокпини** <br/> |
   

