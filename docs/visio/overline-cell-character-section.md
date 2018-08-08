---
title: Ячейка Overline (раздел "Символ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251728
localization_priority: Normal
ms.assetid: 102cce17-43ee-e313-3412-a72d6ee18fe6
description: Определяет, есть ли текст линия над текстом.
ms.openlocfilehash: 3ceb0f5bcb6f66098938e49ea5f176921d0c9808
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814323"
---
# <a name="overline-cell-character-section"></a>Ячейка Overline (раздел "Символ")

Определяет, есть ли текст линия над текстом.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Текст имеет линия над текстом.  <br/> |
|FALSE  <br/> |Текст не имеет линия над текстом.  <br/> |
   
## <a name="remarks"></a>Замечания

Можно также задать значение ячейки, используя диалоговое окно " **текст** " (на вкладке **Главная** щелкните стрелку **шрифтов** ). 
  
Для получения ссылки на ячейки надчеркивание по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |Char.Overline [ *i* ] где *i* < 1 > = 2. 3...  <br/> |
   
Для получения ссылки на ячейки надчеркивание по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionCharacter** <br/> |
|Индекс строки:  <br/> |**visRowCharacter** +  *i* где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visCharacterOverline** <br/> |
   

