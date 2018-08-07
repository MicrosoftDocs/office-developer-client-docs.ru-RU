---
title: Ячейка Font (раздел "Символ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm390
localization_priority: Normal
ms.assetid: 935760a9-307e-90bc-c301-d04283d97427
description: Представляет номер шрифта, используемого для форматирования текста. Номера шрифтов зависят шрифты, установленные в системе. Значение 0 указывает на шрифта по умолчанию, обычно Arial.
ms.openlocfilehash: cbbf2a2400c995e0cbc217c1161fbd18f7459b28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813787"
---
# <a name="font-cell-character-section"></a>Ячейка Font (раздел "Символ")

Представляет номер шрифта, используемого для форматирования текста. Номера шрифтов зависят шрифты, установленные в системе. Значение 0 указывает на шрифта по умолчанию, обычно Arial.
  
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки шрифта по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Char.Font [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки шрифта по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionCharacter** <br/> |
| Индекс строки:  <br/> |**visRowCharacter** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visCharacterFont** <br/> |
   

