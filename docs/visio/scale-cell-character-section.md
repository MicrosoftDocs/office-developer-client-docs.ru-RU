---
title: Ячейка шкалы (раздел знаков)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm870
localization_priority: Normal
ms.assetid: d6fe2574-b719-f38e-b1f1-592a812f1682
description: Определяет ширину шрифта. Значение по умолчанию для этой ячейке составляет 100%.
ms.openlocfilehash: fedbc0aec23320d03ca358f34babda56eaab31e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814725"
---
# <a name="scale-cell-character-section"></a>Ячейка шкалы (раздел знаков)

Определяет ширину шрифта. Значение по умолчанию для этой ячейке составляет 100%.
  
## <a name="remarks"></a>Замечания

Задайте процентную долю от 1 до 99% для уменьшения ширины шрифта. Задайте его от 101% до 600%, чтобы увеличить ширину шрифта.
  
Можно также задать значение ячейки, используя диалоговое окно " **текст** " (на вкладке **Главная** щелкните стрелку **шрифтов** ). 
  
Для получения ссылки на ячейки масштаба по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |Char.FontScale [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки масштаба по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionCharacter** <br/> |
|Индекс строки:  <br/> |**visRowCharacter** +  *i* где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visCharacterFontScale** <br/> |
   
