---
title: Ячейка TextBkgnd (раздел "Формат текстового блока")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251267
localization_priority: Normal
ms.assetid: a238bf1c-1acd-eacd-22f3-a48acaaa4549
description: Определяет цвет фона текста для фигуры.
ms.openlocfilehash: 2256a4c89812924af820c020c225f4b82b1d4856
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815018"
---
# <a name="textbkgnd-cell-text-block-format-section"></a>Ячейка TextBkgnd (раздел "Формат текстового блока")

Определяет цвет фона текста для фигуры.
  
## <a name="remarks"></a>Замечания

Ячейка TextBkgnd может иметь любое значение от 0 до 24 или 255. 0 до 255 ( *visTxtBlklOpaque*), то это означает фон прозрачным текста. 
  
Чтобы ввести другой цвет, используйте функции RGB или HSL, а также один — например, RGB (255,127,255) + 1. Настраиваемые цвета значение цвета RGB, а RGB ( *r, g, b*) + 1, а не числа, будут отображаться в окне таблицы свойств фигуры. При использовании в операции, настраиваемые цвета имеют значения 25 и выше. 
  
Можно задать прозрачность цвет фона текст в ячейке TextBkgndTrans.
  
Чтобы получить ссылку на ячейку TextBkgnd по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |TextBkgnd  <br/> |
   
Для получения ссылки на ячейки TextBkgnd по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowText** <br/> |
|Индекс ячейки:  <br/> |**visTxtBlkBkgnd** <br/> |
   

