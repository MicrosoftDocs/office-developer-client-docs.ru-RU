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
description: Задает поле в нижней части печатной страницы.
ms.openlocfilehash: f546d89b8761c6c1b7340af69d2b48f16c180767
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334414"
---
# <a name="pagebottommargin-cell-print-properties-section"></a>PageBottomMargin Cell (Print Properties Section)

Задает поле в нижней части печатной страницы.
  
## <a name="remarks"></a>Комментарии

Это значение представляет физические единицы и не затронет единицы масштабирования или рисования. Например, если ячейка имеет значение 0,5 в., это поле составляет 0,5 дюйма, даже если единицы страницы — футы. Если единицы измерения не заданы явным образом, значение по умолчанию равно единицам страницы. 
  
Чтобы получить ссылку на ячейку PageBottomMargin по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | PageBottomMargin  <br/> |
   
Чтобы получить ссылку на ячейку PageBottomMargin по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровпринтпропертиес** <br/> |
| Индекс ячейки:  <br/> |**Виспринтпропертиесботтоммаргин** <br/> |
   

