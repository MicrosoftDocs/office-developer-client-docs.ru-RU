---
title: Ячейка PageLeftMargin (раздел "Свойства печати")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60061
localization_priority: Normal
ms.assetid: 7ecdfc37-c9d4-2fde-ed3e-be81657c24e2
description: Задает поле в левой части печатной страницы.
ms.openlocfilehash: 5fd2c8cd5b18a4baedd355627005b7c5c2df3252
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814330"
---
# <a name="pageleftmargin-cell-print-properties-section"></a>Ячейка PageLeftMargin (раздел "Свойства печати")

Задает поле в левой части печатной страницы.
  
## <a name="remarks"></a>Замечания

Это значение представляет физические единицы и не влияет на масштаб или рисования единиц измерения. Например если эта ячейка имеет значение 0,25 дюйма, это поле будет 0,25 дюйма даже в том случае, если страница указываются футов. Если единицы не указан явно, это значение по умолчанию единицах страницы. 
  
Чтобы получить ссылку на ячейку PageLeftMargin по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | PageLeftMargin  <br/> |
   
Для получения ссылки на ячейки PageLeftMargin по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPrintProperties** <br/> |
| Индекс ячейки:  <br/> |**visPrintPropertiesLeftMargin** <br/> |
   

