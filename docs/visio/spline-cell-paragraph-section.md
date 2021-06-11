---
title: SpLine Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm970
localization_priority: Normal
ms.assetid: 84f4e5f1-7c28-9e83-8644-28d117bb10a5
description: Определяет расстояние между одной строкой текста и следующей, выраженной в процентах, где 100% — это высота текстовой строки.
ms.openlocfilehash: 82b2604a62608c0cc4333892d678b1eb886a9c7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434916"
---
# <a name="spline-cell-paragraph-section"></a>SpLine Cell (Paragraph Section)

Определяет расстояние между одной строкой текста и следующей, выраженной в процентах, где 100% — это высота текстовой строки.
  
|**Значение**|**Описание**|
|:-----|:-----|
| \>0  <br/> | Абсолютный интервал, независимо от размера шрифта  <br/> |
| =0  <br/> | Установите сплошной (интервал = 100% от размера шрифта)  <br/> |
| \<0  <br/> | Процент размера шрифта (например, -120% дает 120% интервала)  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку SpLine по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Пара. SpLine  *[i],*  где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку SpLine по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionParagraph** <br/> |
| Индекс строки:  <br/> |**visRowParagraph**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
| Индекс ячейки:  <br/> |**visSpaceLine** <br/> |
   

