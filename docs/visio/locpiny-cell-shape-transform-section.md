---
title: LocPinY Cell (Shape Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm685
localization_priority: Normal
ms.assetid: a29c5d4e-d3d6-d984-495a-4b0b130352ef
description: 'Представляет координату центра вращения фигуры по оси y относительно начала координат фигуры. По умолчанию для определения LocPinY используется следующая формула:'
ms.openlocfilehash: e65bfec8fdcf2be1ee92c23b7afcb183c95ea9fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410597"
---
# <a name="locpiny-cell-shape-transform-section"></a>LocPinY Cell (Shape Transform Section)

Представляет координату центра вращения фигуры по *оси y* относительно начала координат фигуры. По умолчанию для определения LocPinY используется следующая формула: 
  
= Высота \* 0,5
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку LocPinY по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LocPinY  <br/> |
   
Чтобы получить ссылку на ячейку LocPinY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**висровксформаут** <br/> |
| Индекс ячейки:  <br/> |**висксформлокпини** <br/> |
   

