---
title: TheText Cell (Events Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1005
localization_priority: Normal
ms.assetid: 2d63768e-afdb-4b3f-de49-f9ba69ae5391
description: Ячейка события, вычисляемая при изменении текста фигуры или текстовой композиции.
ms.openlocfilehash: 6aa5e14f339d0030d8421eaae62b0e481be91fc7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435168"
---
# <a name="thetext-cell-events-section"></a>TheText Cell (Events Section)

Ячейка события, вычисляемая при изменении текста фигуры или текстовой композиции.
  
## <a name="remarks"></a>Примечания

Ячейки событий оцениваются только при возникновении события, а не при вводе формул. Вы можете использовать ячейку TheText для запуска пересчета, например для пересчета ширины и высоты текста с помощью функций TEXTWIDTH () и TEXTHEIGHT ().
  
Чтобы получить ссылку на ячейку TheText по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | TheText  <br/> |
   
Чтобы получить ссылку на ячейку TheText по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**висровевент** <br/> |
| Индекс ячейки:  <br/> |**висевтцеллсетекст** <br/> |
   

