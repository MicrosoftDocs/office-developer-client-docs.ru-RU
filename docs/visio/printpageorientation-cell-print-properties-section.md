---
title: Ячейка PrintPageOrientation (раздел "Свойства печати")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033795
localization_priority: Normal
ms.assetid: f8354d0d-0ce2-fb33-ddf7-611a2c24a8be
description: Определяет, будет ли страницы при печати книжная или альбомная ориентация.
ms.openlocfilehash: 2adc7dadcb3702e6c5307bb569b2ae1df7aee54e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814492"
---
# <a name="printpageorientation-cell-print-properties-section"></a>Ячейка PrintPageOrientation (раздел "Свойства печати")

Определяет, будет ли страницы при печати книжная или альбомная ориентация.
  
|**Значение**|**Ориентация**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | То же, что принтера  <br/> |**visPPOSameAsPrinter** <br/> |
| 1  <br/> | Книжная  <br/> |**visPPOPortrait** <br/> |
|2  <br/> |Альбомная  <br/> |**visPPOLandscape** <br/> |
   
## <a name="remarks"></a>Замечания

При добавлении новых страниц в документе, этот параметр по умолчанию параметр на активной странице.
  
Чтобы получить ссылку на ячейку PrintPageOrientation по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | PrintPageOrientation  <br/> |
   
Для получения ссылки на ячейки PrintPageOrientation по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPrintProperties** <br/> |
| Индекс ячейки:  <br/> |**visPrintPropertiesPageOrientation** <br/> |
   

