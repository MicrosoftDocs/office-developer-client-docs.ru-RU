---
title: Ячейка DoubleULine (раздел "Символ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm260
localization_priority: Normal
ms.assetid: c18955c8-d653-c29d-d3da-9d3cd0241e17
description: Определяет, есть ли диапазон текста двойного подчеркивания под ней.
ms.openlocfilehash: d0a07d8c86bd7e9ed3eb14074dda164f82c92475
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813654"
---
# <a name="doubleuline-cell-character-section"></a>Ячейка DoubleULine (раздел "Символ")

Определяет, есть ли диапазон текста двойного подчеркивания под ней.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Текст имеет двойное подчеркивание под ней.  <br/> |
|FALSE  <br/> |Текст не имеет двойное подчеркивание под ней.  <br/> |
   
## <a name="remarks"></a>Замечания

Ячейка DoubleULine содержит сведения о форматировании применяется поддиапазона текстом фигуры в том случае, если в разделе символов содержит несколько строк. В противном случае содержит сведения о форматировании для всех текста фигуры.
  
Можно также задать значение ячейки с помощью диалогового окна **текста** (щелкните стрелку **шрифта** на вкладке **Главная** ). 
  
Чтобы получить ссылку на ячейку DoubleULine по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |Char.DblUnderline [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки DoubleULine по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionCharacter** <br/> |
|Индекс строки:  <br/> |**visRowCharacter** +  *i* где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visCharacterDblUnderline** <br/> |
   

