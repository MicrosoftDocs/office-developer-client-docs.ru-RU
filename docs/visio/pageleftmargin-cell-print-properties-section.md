---
title: PageLeftMargin Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60061
localization_priority: Normal
ms.assetid: 7ecdfc37-c9d4-2fde-ed3e-be81657c24e2
description: Указывает поле слева от печатной страницы.
ms.openlocfilehash: 289bd0bf16c6dcd9b26ec1a8c7920a29dab724a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435672"
---
# <a name="pageleftmargin-cell-print-properties-section"></a>PageLeftMargin Cell (Print Properties Section)

Указывает поле слева от печатной страницы.
  
## <a name="remarks"></a>Примечания

Это значение представляет физические единицы и не влияет на единицы масштабирования или рисования. Например, если эта ячейка имеет значение 0,25 дюйма, эта разница составляет 0,25 дюйма, даже если блоки страниц являются ногами. Если единицы явно не заявлены, это значение по умолчанию передается на страницы. 
  
Чтобы получить ссылку на ячейку PageLeftMargin по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | PageLeftMargin  <br/> |
   
Чтобы получить ссылку на ячейку PageLeftMargin по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPrintProperties** <br/> |
| Индекс ячейки:  <br/> |**visPrintPropertiesLeftMargin** <br/> |
   

