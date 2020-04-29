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
description: Определяет цвет, используемый для переднего плана (штриха) узора заливки тени фигуры.
ms.openlocfilehash: 602df83dcb88d4137b0609f9a8b1084a40148a10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422252"
---
# <a name="shdwforegnd-cell-fill-format-section"></a>ShdwForegnd Cell (Fill Format Section)

Определяет цвет, используемый для переднего плана (штриха) узора заливки тени фигуры.
  
## <a name="remarks"></a>Примечания

Чтобы задать цвет, введите число в диапазоне от 0 до 23, которое представляет собой индекс в наборе цветов.
  
Чтобы ввести настраиваемый цвет, используйте функцию RGB или HSL. Значение настраиваемого цвета — это цвет RGB, а RGB ( *r, g, b*), а не число, будут отображаться в окне таблицы свойств фигуры. При использовании в числовых операциях дополнительные цвета имеют значения 24 и выше. 
  
Вы можете задать прозрачность цвета переднего плана для узорной заливки тени фигуры в ячейке ShdwForegndTrans.
  
Чтобы получить ссылку на ячейку ShdwForegnd по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | ShdwForegnd  <br/> |
   
Чтобы получить ссылку на ячейку ShdwForegnd по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**висровфилл** <br/> |
| Индекс ячейки:  <br/> |**висфиллшдвфорегнд** <br/> |
   

