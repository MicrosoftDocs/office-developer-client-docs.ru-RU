---
title: Ячейка Sharpen (раздел "Свойства изображения")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm910
localization_priority: Normal
ms.assetid: aa2bebfc-a6bb-a6b3-3ae9-8553f96b5738
description: 'Повышает резкость точечного рисунка. Значение по умолчанию: 0%. Резкость изображения достигается путем увеличения контрастности смежных пикселов.'
ms.openlocfilehash: fbc66f8c88cde67ad1f259f8392f6d3bd0457be7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814822"
---
# <a name="sharpen-cell-image-properties-section"></a>Ячейка Sharpen (раздел "Свойства изображения")

Повышает резкость точечного рисунка. Значение по умолчанию: 0%. Резкость изображения достигается путем увеличения контрастности смежных пикселов.
  
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки резкость по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Резкость  <br/> |
   
Для получения ссылки на ячейки резкость по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowImage** <br/> |
| Индекс ячейки:  <br/> |**visImageSharpen** <br/> |
   

