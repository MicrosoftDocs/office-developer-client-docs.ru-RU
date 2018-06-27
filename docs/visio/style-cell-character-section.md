---
title: Стиль ячейки (раздел знаков)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251249
localization_priority: Normal
ms.assetid: 4372f1e1-f0a9-2f63-ff79-58f2afdceed5
description: Отображает формат символов, применяемый к диапазону текста в блоке текста фигуры.
ms.openlocfilehash: 48bda5eb798f439e2616b2b910d7ec5ac719d060
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814946"
---
# <a name="style-cell-character-section"></a>Стиль ячейки (раздел знаков)

Отображает формат символов, применяемый к диапазону текста в блоке текста фигуры.
  
|**Стиль**|**Значение**|**Константа автоматизации**|
|:-----|:-----|:-----|
| Полужирный  <br/> | &amp;H1  <br/> |**visBold** <br/> |
| Курсив  <br/> | &amp;H2  <br/> |**visItalic** <br/> |
| Подчеркивание  <br/> | &amp;H4  <br/> |**visUnderLine** <br/> |
| Малые прописные  <br/> | &amp;H8  <br/> |**visSmallCaps** <br/> |
   
## <a name="remarks"></a>Замечания

Стиль ячейки содержит сведения о форматировании применяется поддиапазона текстом фигуры в том случае, если в разделе символов содержит несколько строк. В противном случае содержит сведения о форматировании для всех текста фигуры.
  
Значение представляет двоичное число, в котором каждый бит указывает стиль знака. Например значение 3 представляет текст, отформатированный в курсивом и полужирным шрифтом. Если значение стиля равно 0, текст обычная или неформатированный. Вы можете проверить для определенного формата, с помощью типа Boolean бит\* функции. Обратитесь к документации программирования для получения дополнительных сведений об этих функций.
  
Чтобы получить ссылку на стиль ячейки по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Char.Style [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки стиль по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionCharacter** <br/> |
| Индекс строки:  <br/> |**visRowCharacter** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visCharacterStyle** <br/> |
   
 *Пример* 
  
Предположим, что цвета ячеек в первой строке раздел знаков фигуры задано значение эту формулу:
  
= IF(BITAND(Char.Style,1)=1,4,3)
  
Если заглавной фигуры текст полужирным шрифтом, текст, к которому применяется первой строки свойства символ будет синий (4); в противном случае будет отображаться зеленым цветом (3). В этом примере предполагается, что цвета по умолчанию вступают в силу.
  
Ниже приведен пример настройки стилей ячеек в программу. Первый оператор ссылается на ячейку стиль по имени, а вторая инструкция ссылается на ячейку стиль по индексу. Оба italic особенности текст, к которому применяется второй строке раздел знаков фигуры.
  
