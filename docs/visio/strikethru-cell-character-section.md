---
title: Ячейка Strikethru (раздел "Символ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm975
localization_priority: Normal
ms.assetid: b03b4415-0b1a-eb03-2b5e-373b39a0f07a
description: Определяет, является ли текст зачеркивание.
ms.openlocfilehash: 2b25d1d9b00d062214c02c3fc7b14569b43a5110
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814962"
---
# <a name="strikethru-cell-character-section"></a>Ячейка Strikethru (раздел "Символ")

Определяет, является ли текст зачеркивание.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Текст форматируется как зачеркивание.  <br/> |
|FALSE  <br/> |Текст не формате зачеркивание.  <br/> |
   
## <a name="remarks"></a>Замечания

Можно также задать значение ячейки, используя диалоговое окно " **текст** " (на вкладке **Главная** щелкните стрелку **шрифтов** ). 
  
Чтобы получить ссылку на ячейку Strikethru по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |Char.Strikethru [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки Strikethru по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionCharacter** <br/> |
|Индекс строки:  <br/> |**visRowCharacter** +  *i* где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visCharacterStrikethru** <br/> |
   

