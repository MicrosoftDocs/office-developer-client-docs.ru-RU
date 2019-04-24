---
title: EventMultiDrop Cell (Events Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: caa86e33d0d7aa9ca31cbbf8939e17b581877669
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337193"
---
# <a name="eventmultidrop-cell-events-section"></a>EventMultiDrop Cell (Events Section)

Ячейка события, вычисляемая при разрыве нескольких фигур на странице документа либо в виде экземпляров, либо при копировании или вставке фигур.
  
Ячейки событий оцениваются только при возникновении события, а не при вводе формул.
  
Чтобы сослаться на ячейку EventMultiDrop по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |EventMultiDrop  <br/> |
   
Чтобы сослаться на ячейку EventMultiDrop по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**Висровевент** <br/> |
|Индекс ячейки:  <br/> |**Висевтцеллмултидроп** <br/> |
   

