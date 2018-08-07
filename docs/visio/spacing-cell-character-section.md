---
title: Ячейка Spacing (раздел "Символ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm955
localization_priority: Normal
ms.assetid: 46feb136-01ac-1303-66ab-d772c0ec41a0
description: Управляет дискового пространства между двумя или более символов. Пространство можно добавляются или удаляются с шагом 1/20 точки.
ms.openlocfilehash: ee714306e22cafb7f6d805851a6f977e93172377
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814929"
---
# <a name="spacing-cell-character-section"></a>Ячейка Spacing (раздел "Символ")

Управляет дискового пространства между двумя или более символов. Пространство можно добавляются или удаляются с шагом 1/20 точки.
  
## <a name="remarks"></a>Замечания

Можно также задать значение ячейки, используя диалоговое окно " **текст** " (на вкладке **Главная** щелкните стрелку **шрифтов** ). 
  
Для получения ссылки на ячейки интервал по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |Char.Letterspace [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки интервал по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionCharacter** <br/> |
|Индекс строки:  <br/> |**visRowCharacter** +  *i* где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visCharacterLetterspace** <br/> |
   

