---
title: Spacing Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm955
localization_priority: Normal
ms.assetid: 46feb136-01ac-1303-66ab-d772c0ec41a0
description: Управляет количеством пространства между двумя или более символами. Пространство можно добавлять или вычитать в 1/20-й точке приращений.
ms.openlocfilehash: 927b6203b81af453411cdd13b6f8c8342507a61b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430065"
---
# <a name="spacing-cell-character-section"></a>Spacing Cell (Character Section)

Управляет количеством пространства между двумя или более символами. Пространство можно добавлять или вычитать в 1/20-й точке приращений.
  
## <a name="remarks"></a>Примечания

Вы также можете установить значение этой ячейки с помощью диалогового окна **Text** (на вкладке **Главная** щелкните **стрелку Шрифта).** 
  
Чтобы получить ссылку на ячейку Spacing по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Char.Letterspace[ *i*  ] где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку Spacing по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionCharacter** <br/> |
|Индекс строки:  <br/> |**visRowCharacter**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
|Индекс ячейки:  <br/> |**visCharacterLetterspace** <br/> |
   

