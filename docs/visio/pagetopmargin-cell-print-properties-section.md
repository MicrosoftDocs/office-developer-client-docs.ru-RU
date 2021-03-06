---
title: PageTopMargin Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033785
localization_priority: Normal
ms.assetid: 2ba0fd22-65a6-6cb6-da00-08f391705544
description: Указывает поле в верхней части страницы принтера.
ms.openlocfilehash: ff2bffffed39c5571386e792d2ffc8d20d6b291e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416582"
---
# <a name="pagetopmargin-cell-print-properties-section"></a>PageTopMargin Cell (Print Properties Section)

Указывает поле в верхней части страницы принтера.
  
## <a name="remarks"></a>Примечания

Это значение представляет физические единицы и не влияет на единицы масштабирования или рисования. Например, если эта ячейка имеет значение 0,25 дюйма, эта разница составляет 0,25 дюйма, даже если блоки страниц являются ногами. Если единицы явно не заявлены, это значение по умолчанию передается на страницы. 
  
Чтобы получить ссылку на ячейку PageTopMargin по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | PageTopMargin  <br/> |
   
Чтобы получить ссылку на ячейку PageTopMargin по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPrintProperties** <br/> |
| Индекс ячейки:  <br/> |**visPrintPropertiesTopMargin** <br/> |
   

