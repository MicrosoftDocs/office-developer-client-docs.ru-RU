---
title: Ячейка EventMultiDrop (раздел "События")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: e44cd18c3f7673761f457db9cd4bfe00a8ab89bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813715"
---
# <a name="eventmultidrop-cell-events-section"></a>Ячейка EventMultiDrop (раздел "События")

Ячейка события, которое оценивается при перетаскивании нескольких фигур на странице документа в виде экземпляров или при дублировании или вставке фигур.
  
Событие ячеек вычисляются только в том случае, когда возникает событие, не после ввода формул.
  
Для ссылки на ячейки EventMultiDrop по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |EventMultiDrop  <br/> |
   
Для ссылки на ячейки EventMultiDrop по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowEvent** <br/> |
|Индекс ячейки:  <br/> |**visEvtCellMultiDrop** <br/> |
   

