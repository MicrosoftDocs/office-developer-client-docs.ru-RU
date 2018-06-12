---
title: Ячейка Y (раздел заметки)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60095
localization_priority: Normal
ms.assetid: 527a4615-2013-a4b4-81cd-7f5d71c1803c
description: Y-координата метки комментария, используемой в координаты страницы.
ms.openlocfilehash: cc2399de7919512796a39ca39c705c214f4c51a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815202"
---
# <a name="y-cell-annotation-section"></a>Ячейка Y (раздел заметки)

*Y* -координата метки комментария, используемой в координаты страницы. 
  
> [!NOTE]
> В этой ячейке используется для контроля комментариев только при открытии VSD-файл в Microsoft Visio 2013 или при сохранении файла vsdx (en) в формате .vsd. Он не используется для отслеживания комментариев в документах vsdx (en) в Visio 2013. 
  
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку Y по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Annotation.Y [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки Y по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionAnnotation** <br/> |
| Индекс строки:  <br/> |**visRowAnnotation** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visAnnotationY** <br/> |
   

