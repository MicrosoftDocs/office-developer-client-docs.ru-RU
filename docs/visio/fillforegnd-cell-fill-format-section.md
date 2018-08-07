---
title: Ячейка FillForegnd (раздел "Формат заливки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251241
localization_priority: Normal
ms.assetid: 7548a480-4dce-45e0-281b-f6f8bdf05c0b
description: Определяет цвет, используемый для переднего плана (числу штрихов) узора заливки фигуры.
ms.openlocfilehash: 27126457963e4e55419b0cac5baf1eab08fe3cc6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813769"
---
# <a name="fillforegnd-cell-fill-format-section"></a>Ячейка FillForegnd (раздел "Формат заливки")

Определяет цвет, используемый для переднего плана (числу штрихов) узора заливки фигуры.
  
## <a name="remarks"></a>Замечания

Чтобы задать цвет, введите число от 0 до 23.
  
Чтобы ввести другой цвет, используйте функцию RGB или HSL. Настраиваемые цвета значение цвета RGB, а RGB ( *r, g, b*), а не числа, будут отображаться в окне таблицы свойств фигуры. При использовании в операции, настраиваемые цвета имеют значения из 24 и выше. 
  
Можно задать Прозрачность заливки переднего плана в ячейке FillForegndTrans.
  
Чтобы получить ссылку на ячейку FillForegnd по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |FillForegnd  <br/> |
   
Для получения ссылки на ячейки FillForegnd по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowFill** <br/> |
|Индекс ячейки:  <br/> |**visFillForegnd** <br/> |
   

