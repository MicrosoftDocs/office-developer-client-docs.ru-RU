---
title: PageBottomMargin Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60060
localization_priority: Normal
ms.assetid: 7a97e97c-278d-2e1e-6c4f-f5f32e2cdeb0
description: Указывает поле в нижней части печатной страницы.
ms.openlocfilehash: f546d89b8761c6c1b7340af69d2b48f16c180767
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438598"
---
# <a name="pagebottommargin-cell-print-properties-section"></a>PageBottomMargin Cell (Print Properties Section)

Указывает поле в нижней части печатной страницы.
  
## <a name="remarks"></a>Примечания

Это значение представляет физические единицы и не влияет на единицы масштабирования или рисования. Например, если эта ячейка имеет значение 0,5 дюйма, эта маржа составляет 0,5 дюйма, даже если блоки страниц являются ногами. Если единицы явно не заявлены, это значение по умолчанию передается на страницы. 
  
Чтобы получить ссылку на ячейку PageBottomMargin по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | PageBottomMargin  <br/> |
   
Чтобы получить ссылку на ячейку PageBottomMargin по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPrintProperties** <br/> |
| Индекс ячейки:  <br/> |**visPrintPropertiesBottomMargin** <br/> |
   

