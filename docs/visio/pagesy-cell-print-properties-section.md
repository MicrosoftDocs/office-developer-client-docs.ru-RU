---
title: Ячейка PagesY (раздел "Свойства печати")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033790
localization_priority: Normal
ms.assetid: 396a0f3e-dbbb-3f5b-3c5d-f7dd454a765f
description: Определяет количество печатных страниц для размещения страницы документа по вертикали.
ms.openlocfilehash: 1663fac8efdf06599d1e3c00d5eb0d00ec52e476
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814343"
---
# <a name="pagesy-cell-print-properties-section"></a>Ячейка PagesY (раздел "Свойства печати")

Определяет количество печатных страниц для размещения страницы документа по вертикали. 
  
## <a name="remarks"></a>Замечания

Это значение используется только в том случае, если ячейка OnPage имеет значение TRUE. 
  
Чтобы получить ссылку на ячейку PagesY по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | PagesY  <br/> |
   
Для получения ссылки на ячейки PagesY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPrintProperties** <br/> |
| Индекс ячейки:  <br/> |**visPrintPropertiesPagesY** <br/> |
   

