---
title: LocPinX Cell (Shape Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm680
localization_priority: Normal
ms.assetid: b82feade-5793-8a6e-3ff4-69a4cbdd2cf9
description: 'Представляет координату центра вращения фигуры по оси x относительно начала координат фигуры. По умолчанию для определения LocPinX используется следующая формула:'
ms.openlocfilehash: 2eb5c328eed3c97652173670c426b83b8c358833
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358053"
---
# <a name="locpinx-cell-shape-transform-section"></a>LocPinX Cell (Shape Transform Section)

Представляет координату центра вращения фигуры по *оси x* относительно начала координат фигуры. По умолчанию для определения LocPinX используется следующая формула: 
  
= Ширина \* 0,5
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку LocPinX по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LocPinX  <br/> |
   
Чтобы получить ссылку на ячейку LocPinX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровксформаут** <br/> |
| Индекс ячейки:  <br/> |**Висксформлокпинкс** <br/> |
   

