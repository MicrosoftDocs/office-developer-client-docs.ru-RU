---
title: Scale Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm870
localization_priority: Normal
ms.assetid: d6fe2574-b719-f38e-b1f1-592a812f1682
description: Контролирует ширину шрифта. Значение по умолчанию для этой ячейки составляет 100%.
ms.openlocfilehash: 60e896772ddd1d59e1a1da7f2c0e90893658c624
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429154"
---
# <a name="scale-cell-character-section"></a>Scale Cell (Character Section)

Контролирует ширину шрифта. Значение по умолчанию для этой ячейки составляет 100%.
  
## <a name="remarks"></a>Примечания

Установите процент от 1% до 99%, чтобы уменьшить ширину шрифта. Установите его между 101% и 600% для увеличения ширины шрифта.
  
Вы также можете установить значение этой ячейки с помощью диалогового окна **Text** (на вкладке **Главная** щелкните **стрелку Шрифта).** 
  
Чтобы получить ссылку на ячейку Scale по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Char.FontScale[i] где *i* = <1>, 2, 3...   <br/> |
   
Чтобы получить ссылку на ячейку Scale по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionCharacter** <br/> |
|Индекс строки:  <br/> |**visRowCharacter**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
|Индекс ячейки:  <br/> |**visCharacterFontScale** <br/> |
   

