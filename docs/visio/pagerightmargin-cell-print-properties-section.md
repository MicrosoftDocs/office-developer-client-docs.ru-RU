---
title: PageRightMargin Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60062
localization_priority: Normal
ms.assetid: f864c759-ed94-8ab7-d664-cc04b3ed743e
description: Указывает поле справа от печатной страницы.
ms.openlocfilehash: d30669626fe07379521d61554010ae1bd7b0e83a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33440012"
---
# <a name="pagerightmargin-cell-print-properties-section"></a>PageRightMargin Cell (Print Properties Section)

Указывает поле справа от печатной страницы.
  
## <a name="remarks"></a>Примечания

Это значение представляет физические единицы и не влияет на масштаб или единицы рисования. Например, если значение этой ячейки составляет 0,25 дюйма, то это поле будет 0,25 дюйма, даже если единицы страниц находятся в метрах. Если единицы не заявимы, это значение по умолчанию занося в единицы страниц. 
  
Чтобы получить ссылку на ячейку PageRightMargin по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | PageRightMargin  <br/> |
   
Чтобы получить ссылку на ячейку PageRightMargin по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPrintProperties** <br/> |
| Индекс ячейки:  <br/> |**visPrintPropertiesRightMargin** <br/> |
   

