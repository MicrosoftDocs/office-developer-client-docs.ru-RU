---
title: Ячейка FillBkgnd (раздел "Формат заливки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm365
localization_priority: Normal
ms.assetid: 603d698f-a025-538c-8767-18e7716a9a5f
description: Определяет цвет, используемый в качестве фона (заливки) узора заливки фигуры.
ms.openlocfilehash: d1222026887313d7737a3a0ded9e798e9bf5ea30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813748"
---
# <a name="fillbkgnd-cell-fill-format-section"></a>Ячейка FillBkgnd (раздел "Формат заливки")

Определяет цвет, используемый в качестве фона (заливки) узора заливки фигуры.
  
## <a name="remarks"></a>Замечания

Чтобы задать цвет, введите число от 0 до 23.
  
Чтобы ввести другой цвет, используйте функцию RGB или HSL. Настраиваемые цвета значение цвета RGB, а RGB (*r, g, b*), а не числа, будут отображаться в окне таблицы свойств фигуры. При использовании в операции, настраиваемые цвета имеют значения из 24 и выше. 
  
Можно задать Прозрачность заливки фона в ячейке FillBkgndTrans. 
  
Чтобы получить ссылку на ячейку FillBkgnd по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | FillBkgnd  <br/> |
   
Для получения ссылки на ячейки FillBkgnd по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowFill** <br/> |
| Индекс ячейки:  <br/> |**visFillBkgnd** <br/> |
   

