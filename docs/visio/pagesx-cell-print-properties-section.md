---
title: Ячейка PagesX (раздел "Свойства печати")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60064
localization_priority: Normal
ms.assetid: a10bf4c2-24f4-4c53-39ba-2b8cd5b50d2c
description: Определяет количество печатных страниц для размещения страницы документа по горизонтали.
ms.openlocfilehash: 4f1cf3286e7b54dc90925bf2f1ab9fe8532022e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814350"
---
# <a name="pagesx-cell-print-properties-section"></a>Ячейка PagesX (раздел "Свойства печати")

Определяет количество печатных страниц для размещения страницы документа по горизонтали. 
  
## <a name="remarks"></a>Замечания

Это значение используется только в том случае, если ячейка OnPage имеет значение TRUE. 
  
Чтобы получить ссылку на ячейку PagesX по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | PagesX  <br/> |
   
Для получения ссылки на ячейки PagesX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPrintProperties** <br/> |
| Индекс ячейки:  <br/> |**visPrintPropertiesPagesX** <br/> |
   

