---
title: EventMultiDrop Cell (Events Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: caa86e33d0d7aa9ca31cbbf8939e17b581877669
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416722"
---
# <a name="eventmultidrop-cell-events-section"></a>EventMultiDrop Cell (Events Section)

Ячейка события, которая оценивается при отброшении нескольких фигур на страницу рисования в качестве экземпляров или при дублировании или вплеи фигур.
  
Ячейки событий оцениваются только при событии, а не при вводе формулы.
  
Чтобы сослаться на ячейку EventMultiDrop по имени из другой формулы или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |EventMultiDrop  <br/> |
   
Чтобы сослаться на ячейку EventMultiDrop по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowEvent** <br/> |
|Индекс ячейки:  <br/> |**visEvtCellMultiDrop** <br/> |
   

