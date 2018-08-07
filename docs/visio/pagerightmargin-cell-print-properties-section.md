---
title: Ячейка PageRightMargin (раздел "Свойства печати")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60062
localization_priority: Normal
ms.assetid: f864c759-ed94-8ab7-d664-cc04b3ed743e
description: Задает поле в правой части печатной страницы.
ms.openlocfilehash: 951a16ff20e294b68ed5447d330f4e7cbc100c82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814340"
---
# <a name="pagerightmargin-cell-print-properties-section"></a>Ячейка PageRightMargin (раздел "Свойства печати")

Задает поле в правой части печатной страницы.
  
## <a name="remarks"></a>Замечания

Это значение представляет физические единицы и не влияет на масштаб или рисования единиц измерения. Например если эта ячейка имеет значение 0,25 дюйма, это поле будет 0,25 дюйма даже в том случае, если страница указываются футов. Если единицы не указан явно, это значение по умолчанию единицах страницы. 
  
Чтобы получить ссылку на ячейку PageRightMargin по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | PageRightMargin  <br/> |
   
Для получения ссылки на ячейки PageRightMargin по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPrintProperties** <br/> |
| Индекс ячейки:  <br/> |**visPrintPropertiesRightMargin** <br/> |
   

