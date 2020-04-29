---
title: EventDrop Cell (Events Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm350
localization_priority: Normal
ms.assetid: f84afe83-8391-0c13-f442-ea8794b38642
description: Ячейка события, вычисляемая при разрыве фигуры на странице документа либо в виде экземпляра, либо при копировании или вставке фигуры.
ms.openlocfilehash: f1433394dbd58c7c4422c6bca1e79a4f2c8e0c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408595"
---
# <a name="eventdrop-cell-events-section"></a>EventDrop Cell (Events Section)

Ячейка события, вычисляемая при разрыве фигуры на странице документа либо в виде экземпляра, либо при копировании или вставке фигуры.
  
## <a name="remarks"></a>Примечания

Ячейки событий оцениваются только при возникновении события, а не при вводе формул.
  
Чтобы получить ссылку на ячейку EventDrop по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | EventDrop  <br/> |
   
Чтобы получить ссылку на ячейку EventDrop по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**висровевент** <br/> |
| Индекс ячейки:  <br/> |**висевтцеллдроп** <br/> |
   

