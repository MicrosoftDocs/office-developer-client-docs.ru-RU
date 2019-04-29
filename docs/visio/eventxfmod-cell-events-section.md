---
title: EventXFMod Cell (Events Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251313
localization_priority: Normal
ms.assetid: b88588a2-c651-7eab-9c7a-ed78f20d1ba3
description: Ячейка события, вычисляемая при преобразовании позиции или ориентации фигуры на странице (XF).
ms.openlocfilehash: c4ed4ddd9b255a9a52fc81349b514dbd25772c98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418535"
---
# <a name="eventxfmod-cell-events-section"></a>EventXFMod Cell (Events Section)

Ячейка события, вычисляемая при преобразовании позиции или ориентации фигуры на странице ("XF").
  
## <a name="remarks"></a>Примечания

Ячейки событий оцениваются только при возникновении события, а не при вводе формул.
  
Чтобы получить ссылку на ячейку EventXFMod по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | EventXFMod  <br/> |
   
Чтобы получить ссылку на ячейку EventXFMod по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровевент** <br/> |
| Индекс ячейки:  <br/> |**Висевтцеллксфмод** <br/> |
   

