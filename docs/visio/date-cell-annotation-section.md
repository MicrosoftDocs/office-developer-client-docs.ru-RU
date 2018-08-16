---
title: Ячейка Date (раздел "Примечание")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60036
localization_priority: Normal
ms.assetid: f1f11803-614b-a40d-0a2d-131093e7609e
description: Содержит дату и время последнего изменения комментария.
ms.openlocfilehash: 4b6e7ea70302b10728d82f36ad0db39077af9523
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813558"
---
# <a name="date-cell-annotation-section"></a>Ячейка Date (раздел "Примечание")

Содержит дату и время последнего изменения комментария. 
  
> [!NOTE]
> В этой ячейке используется для контроля комментариев только при открытии VSD-файл в Microsoft Visio 2013 или при сохранении файла vsdx (en) в формате .vsd. Он не используется для отслеживания комментариев в документах vsdx (en) в Visio 2013. 
  
## <a name="remarks"></a>Замечания

В поле комментария в пользовательском интерфейсе отображается только дата.
  
Для получения ссылки на ячейки даты по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Annotation.Date [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки даты по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionAnnotation** <br/> |
| Индекс строки:  <br/> |**visRowAnnotation** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visAnnotationDate** <br/> |
   
