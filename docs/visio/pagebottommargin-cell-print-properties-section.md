---
title: Ячейка PageBottomMargin (печати Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60060
localization_priority: Normal
ms.assetid: 7a97e97c-278d-2e1e-6c4f-f5f32e2cdeb0
description: Задает поле в нижней части печатной страницы.
ms.openlocfilehash: fb67cf87f5e50719d24b0f354acc93209eed8811
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814329"
---
# <a name="pagebottommargin-cell-print-properties-section"></a>Ячейка PageBottomMargin (печати Properties Section)

Задает поле в нижней части печатной страницы.
  
## <a name="remarks"></a>Замечания

Это значение представляет физические единицы и не влияет на масштаб или рисования единиц измерения. Например если эта ячейка имеет значение 0,5 дюйма, это поле будет 0,5 дюйма даже в том случае, если страница указываются футов. Если единицы не указан явно, это значение по умолчанию единицах страницы. 
  
Чтобы получить ссылку на ячейку PageBottomMargin по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | PageBottomMargin  <br/> |
   
Для получения ссылки на ячейки PageBottomMargin по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPrintProperties** <br/> |
| Индекс ячейки:  <br/> |**visPrintPropertiesBottomMargin** <br/> |
   

