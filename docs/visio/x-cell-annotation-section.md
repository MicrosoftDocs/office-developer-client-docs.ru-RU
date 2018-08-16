---
title: Ячейка X (раздел "Заметка")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1028735
localization_priority: Normal
ms.assetid: f9db8623-9fcf-7037-2d11-d509f463025d
description: Представляет x-координату знака примечания в координатах страницы.
ms.openlocfilehash: 454c28c6f15c705148155751d533a516aae7d2d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815176"
---
# <a name="x-cell-annotation-section"></a>Ячейка X (раздел "Заметка")

Представляет *x*-координату знака примечания в координатах страницы. 
  
> [!NOTE]
> Эта ячейка используется для отслеживания комментариев только при открытии VSD-файла в Microsoft Visio 2013 или при сохранении VSDX-файла в формате VSD-файла. Она не используется для отслеживания комментариев в VSDX-документах в Visio 2013. 
  
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку X по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Annotation.X[  *i*  ], где *i* = <1>, 2, 3…  <br/> |
   
Чтобы получить ссылку на ячейку X по индексу из программы, укажите свойство **CellsSRC** с такими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionAnnotation** <br/> |
| Индекс строки:  <br/> |**visRowAnnotation** +  *i*, где *i* = 0, 1, 2…  <br/> |
| Индекс ячейки:  <br/> |**visAnnotationX** <br/> |
   

