---
title: ShdwForegnd Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251244
localization_priority: Normal
ms.assetid: ea153390-631d-79fd-c1ba-4c281239a24e
description: Определяет цвет, используемый для переднего плана (хода) шаблона заливки теней формы.
ms.openlocfilehash: 602df83dcb88d4137b0609f9a8b1084a40148a10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422252"
---
# <a name="shdwforegnd-cell-fill-format-section"></a>ShdwForegnd Cell (Fill Format Section)

Определяет цвет, используемый для переднего плана (хода) шаблона заливки теней формы.
  
## <a name="remarks"></a>Примечания

Чтобы установить цвет, введите число от 0 до 23, которое является индексом в коллекцию цветов.
  
Чтобы ввести настраиваемый цвет, используйте функцию RGB или HSL. Значение настраиваемого цвета — это цвет RGB, и RGB *(r, g, b),* а не номер будет показан в окне ShapeSheet. Пользовательские цвета, используемые в числовом режиме, имеют значения 24 и выше. 
  
В ячейке ShdwForegndTrans можно задать прозрачность цвета переднего плана шаблона теневого заполнения фигуры.
  
Чтобы получить ссылку на ячейку ShdwForegnd по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | ShdwForegnd  <br/> |
   
Чтобы получить ссылку на ячейку ShdwForegnd по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowFill** <br/> |
| Индекс ячейки:  <br/> |**visFillShdwForegnd** <br/> |
   

