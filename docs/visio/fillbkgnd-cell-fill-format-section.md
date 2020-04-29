---
title: FillBkgnd Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm365
localization_priority: Normal
ms.assetid: 603d698f-a025-538c-8767-18e7716a9a5f
description: Определяет цвет, используемый для фона (заливки) узора заливки фигуры.
ms.openlocfilehash: f4df5d2b44a50380c996b9b2e0f7cda7d212093b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436645"
---
# <a name="fillbkgnd-cell-fill-format-section"></a>FillBkgnd Cell (Fill Format Section)

Определяет цвет, используемый для фона (заливки) узора заливки фигуры.
  
## <a name="remarks"></a>Примечания

Чтобы задать цвет, введите число от 0 до 23.
  
Чтобы ввести настраиваемый цвет, используйте функцию RGB или HSL. Значение настраиваемого цвета — это цвет RGB, а RGB (*r, g, b*), а не число, будут отображаться в окне таблицы свойств фигуры. При использовании в числовых операциях дополнительные цвета имеют значения 24 и выше. 
  
Вы можете задать прозрачность фоновой заливки в ячейке FillBkgndTrans. 
  
Чтобы получить ссылку на ячейку FillBkgnd по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | FillBkgnd  <br/> |
   
Чтобы получить ссылку на ячейку FillBkgnd по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**висровфилл** <br/> |
| Индекс ячейки:  <br/> |**висфиллбкгнд** <br/> |
   

