---
title: Ячейка PageTopMargin (раздел "Свойства печати")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033785
localization_priority: Normal
ms.assetid: 2ba0fd22-65a6-6cb6-da00-08f391705544
description: Задает поле в верхней части страницы принтера.
ms.openlocfilehash: 1b7be63e3f21365231120c602d8edfe1dc727f88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814346"
---
# <a name="pagetopmargin-cell-print-properties-section"></a>Ячейка PageTopMargin (раздел "Свойства печати")

Задает поле в верхней части страницы принтера.
  
## <a name="remarks"></a>Замечания

Это значение представляет физические единицы и не влияет на масштаб или рисования единиц измерения. Например если эта ячейка имеет значение 0,25 дюйма, это поле будет 0,25 дюйма даже в том случае, если страница указываются футов. Если единицы не указан явно, это значение по умолчанию единицах страницы. 
  
Чтобы получить ссылку на ячейку PageTopMargin по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | PageTopMargin  <br/> |
   
Для получения ссылки на ячейки PageTopMargin по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPrintProperties** <br/> |
| Индекс ячейки:  <br/> |**visPrintPropertiesTopMargin** <br/> |
   

