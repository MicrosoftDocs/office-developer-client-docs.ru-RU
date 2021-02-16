---
title: FillForegnd Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251241
localization_priority: Normal
ms.assetid: 7548a480-4dce-45e0-281b-f6f8bdf05c0b
description: Определяет цвет, используемый для переднего плана (росчерка) шаблона заливки фигуры.
ms.openlocfilehash: 352fecf8d99069cfb5ebd72d295284dc03446364
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415567"
---
# <a name="fillforegnd-cell-fill-format-section"></a>FillForegnd Cell (Fill Format Section)

Определяет цвет, используемый для переднего плана (росчерка) шаблона заливки фигуры.
  
## <a name="remarks"></a>Примечания

Чтобы установить цвет, введите число от 0 до 23.
  
Чтобы ввести пользовательский цвет, используйте функцию RGB или HSL. Значением пользовательского цвета является цвет RGB, и RGB( *r, g, b*), а не число, будет показано в окне ShapeSheet. При работе с числами пользовательские цвета имеют значения 24 и выше. 
  
Вы можете установить прозрачность заполнения переднего плана в ячейке FillForegndTrans.
  
Чтобы получить ссылку на ячейку FillForegnd по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |FillForegnd  <br/> |
   
Чтобы получить ссылку на ячейку FillForegnd по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowFill** <br/> |
|Индекс ячейки:  <br/> |**visFillForegnd** <br/> |
   

