---
title: Ячейка Color (раздел "Символ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm160
localization_priority: Normal
ms.assetid: 1c9aab2e-6c2f-0684-4e66-c35ac71883d6
description: Определяет цвет, используемый для текста фигуры.
ms.openlocfilehash: ef07f4165882e08a2292e4ee549f8807fe8403e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813384"
---
# <a name="color-cell-character-section"></a>Ячейка Color (раздел "Символ")

Определяет цвет, используемый для текста фигуры.
  
## <a name="remarks"></a>Замечания

Чтобы задать цвет, введите число от 0 до 23.
  
Чтобы ввести другой цвет, используйте функцию RGB или HSL. Настраиваемые цвета значение цвета RGB, а RGB ( *r, g, b*), а не числа, будут отображаться в окне таблицы свойств фигуры. При использовании в операции, настраиваемые цвета имеют значения из 24 и выше. 
  
Можно задать прозрачность цвет текста в ячейку прозрачность.
  
Для получения ссылки на ячейки цвет по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |Char.Color [ *i* ] где *i* = < 1 > 2, 3,...  <br/> |
   
Для получения ссылки на ячейки цвет по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionCharacter** <br/> |
|Индекс строки:  <br/> |**visRowCharacter** +  *i* где *i* = 0, 1, 2,...  <br/> |
|Индекс ячейки:  <br/> |**visCharacterColor** <br/> |
   

