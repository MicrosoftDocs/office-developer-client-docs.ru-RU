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
description: Определяет цвет, используемый для переднего плана (росчерка) шаблона заливки тени для перепада фигуры.
ms.openlocfilehash: 602df83dcb88d4137b0609f9a8b1084a40148a10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422252"
---
# <a name="shdwforegnd-cell-fill-format-section"></a>ShdwForegnd Cell (Fill Format Section)

Определяет цвет, используемый для переднего плана (росчерка) шаблона заливки тени для перепада фигуры.
  
## <a name="remarks"></a>Примечания

Чтобы установить цвет, введите число от 0 до 23, которое является индексом в коллекцию цветов.
  
Чтобы ввести пользовательский цвет, используйте функцию RGB или HSL. Значением пользовательского цвета является цвет RGB, и RGB( *r, g, b*), а не число, будет показано в окне ShapeSheet. При работе с числами пользовательские цвета имеют значения 24 и выше. 
  
Вы можете установить прозрачность цвета переднего плана шаблона заливки теней фигуры в ячейке ShdwForegndTrans.
  
Чтобы получить ссылку на ячейку ShdwForegnd по имени из другой формулы или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | ShdwForegnd  <br/> |
   
Чтобы получить ссылку на ячейку ShdwForegnd по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowFill** <br/> |
| Индекс ячейки:  <br/> |**visFillShdwForegnd** <br/> |
   

