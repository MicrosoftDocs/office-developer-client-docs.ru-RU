---
title: TextBkgnd Cell (Text Block Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251267
localization_priority: Normal
ms.assetid: a238bf1c-1acd-eacd-22f3-a48acaaa4549
description: Определяет цвет фона текста для фигуры.
ms.openlocfilehash: 2450bf0cb0e013c0f9310eacfca0f5a20e7e6063
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406544"
---
# <a name="textbkgnd-cell-text-block-format-section"></a>TextBkgnd Cell (Text Block Format Section)

Определяет цвет фона текста для фигуры.
  
## <a name="remarks"></a>Примечания

Ячейка TextBkgnd может иметь любое значение в диапазоне от 0 до 24 или 255. Значения 0 и 255 ( *висткстблклопакуе*) указывают на прозрачный фон текста. 
  
Чтобы ввести настраиваемый цвет, используйте функцию RGB или HSL, а другую — например, RGB (255127255) + 1. Значением настраиваемого цвета является цвет RGB, а RGB ( *r, g, b*) + 1, а не число, будет отображаться в окне таблицы свойств фигуры. При использовании в числовых операциях дополнительные цвета имеют значения 25 и выше. 
  
Вы можете задать прозрачность цвета фона текста в ячейке TextBkgndTrans.
  
Чтобы получить ссылку на ячейку TextBkgnd по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |TextBkgnd  <br/> |
   
Чтобы получить ссылку на ячейку TextBkgnd по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**Висровтекст** <br/> |
|Индекс ячейки:  <br/> |**Висткстблкбкгнд** <br/> |
   

