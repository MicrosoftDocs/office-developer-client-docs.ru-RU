---
title: EventDblClick Cell (Events Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251312
localization_priority: Normal
ms.assetid: ca949013-f998-1bce-39e5-ac6f68ab2392
description: Ячейка события, вычисляемая при двойном щелчке фигуры.
ms.openlocfilehash: a50e88ecd8e432629e246f7038dfcc9626725cc5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438220"
---
# <a name="eventdblclick-cell-events-section"></a>EventDblClick Cell (Events Section)

Ячейка события, вычисляемая при двойном щелчке фигуры.
  
## <a name="remarks"></a>Примечания

Ячейки событий оцениваются только при возникновении события, а не при вводе формул.
  
Чтобы получить ссылку на ячейку EventDblClick по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | EventDblClick  <br/> |
   
Чтобы получить ссылку на ячейку EventDblClick по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**висровевент** <br/> |
| Индекс ячейки:  <br/> |**висевтцеллдблкликк** <br/> |
   

