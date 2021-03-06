---
title: Color Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm160
localization_priority: Normal
ms.assetid: 1c9aab2e-6c2f-0684-4e66-c35ac71883d6
description: Определяет цвет, используемый для текста фигуры.
ms.openlocfilehash: a27d957781ca9a784e7ab9d5c1ce4f533b9a55ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439991"
---
# <a name="color-cell-character-section"></a>Color Cell (Character Section)

Определяет цвет, используемый для текста фигуры.
  
## <a name="remarks"></a>Примечания

Чтобы установить цвет, введите число от 0 до 23.
  
Чтобы ввести настраиваемый цвет, используйте функцию RGB или HSL. Значение настраиваемого цвета — это цвет RGB, и RGB *(r, g, b),* а не номер будет показан в окне ShapeSheet. Пользовательские цвета, используемые в числовом режиме, имеют значения 24 и выше. 
  
Вы можете установить прозрачность цвета текста в ячейке Transparency.
  
Чтобы получить ссылку на ячейку Color по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |*Char.Color[i]* где *i* = <1>, 2, 3, ...  <br/> |
   
Чтобы получить ссылку на ячейку Color по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionCharacter** <br/> |
|Индекс строки:  <br/> |**visRowCharacter**  +   *i,* *где i* = 0, 1, 2, ...  <br/> |
|Индекс ячейки:  <br/> |**visCharacterColor** <br/> |
   

