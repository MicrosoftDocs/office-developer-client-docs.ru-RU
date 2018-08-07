---
title: Ячейка ScaleY (раздел "Свойства печати")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033788
localization_priority: Normal
ms.assetid: 02835aff-455b-ffeb-d53b-28387b6ce361
description: Указывает процент увеличения страницы документа на странице принтера.
ms.openlocfilehash: 2735b2cfce04cc9a8d8da1a815081aaa5892c723
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814724"
---
# <a name="scaley-cell-print-properties-section"></a>Ячейка ScaleY (раздел "Свойства печати")

Указывает процент увеличения страницы документа на странице принтера.
  
## <a name="remarks"></a>Замечания

Это значение используется только в том случае, если значение ячейки OnPage — FALSE. Ячейки ScaleX и ScaleY всегда с таким же значением, который соответствует значению в параметре **обеспечить, чтобы** на вкладке **Параметры печати** в диалоговом окне " **Параметры страницы** " (на вкладке " **Конструктор** ", щелкните стрелку **Параметры страницы** ). 
  
Для получения ссылки на ячейки ScaleY по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |ScaleY  <br/> |
   
Для получения ссылки на ячейки ScaleY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPrintProperties** <br/> |
|Индекс ячейки:  <br/> |**visPrintPropertiesScaleY** <br/> |
   

