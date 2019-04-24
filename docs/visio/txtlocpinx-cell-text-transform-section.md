---
title: TxtLocPinX Cell (Text Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251275
localization_priority: Normal
ms.assetid: cbfc4e91-10d1-d50e-3e8a-f269f7123276
description: 'Определяет координату x центра вращения блока текста относительно начала блока текста. По умолчанию используется следующая формула:'
ms.openlocfilehash: 390f8129e8000a043969eda0ab1c8e4ef62515ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316452"
---
# <a name="txtlocpinx-cell-text-transform-section"></a>TxtLocPinX Cell (Text Transform Section)

Определяет координату *x* центра вращения блока текста относительно начала блока текста. По умолчанию используется следующая формула: 
  
= TxtWidth \* 0,5
  
Эта формула вычисляется как горизонтальный центр блока текста.
  
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку TxtLocPinX по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | TxtLocPinX  <br/> |
   
Чтобы получить ссылку на ячейку TxtLocPinX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровтекстксформ** <br/> |
| Индекс ячейки:  <br/> |**Висксформлокпинкс** <br/> |
   

