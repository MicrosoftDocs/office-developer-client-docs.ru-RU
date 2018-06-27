---
title: Ячейка OnPage (печати Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033793
localization_priority: Normal
ms.assetid: 4015506a-e24a-0276-c854-7791a7019067
description: Указывает, печатается ли документ на определенное число страниц принтера.
ms.openlocfilehash: 5b695ccf6fa2364809e2f5124b9f55ea6aab50e0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814313"
---
# <a name="onpage-cell-print-properties-section"></a>Ячейка OnPage (печати Properties Section)

Указывает, печатается ли документ на определенное число страниц принтера. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Размещения страницы документа на определенное число печатных страниц.  <br/> |
|FALSE  <br/> |Не соответствуют страницу документа для определенных количество печатных страниц (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Замечания

Если ячейка OnPage задано значение TRUE, Microsoft Visio использует ячейки PagesX и PagesY для определения количество печатных страниц для размещения документа. Значения в ячейках ScaleX и ScaleY игнорируются. Это можно оценить как параметр «autoscale».
  
Это значение соответствует параметру **по размеру** на вкладке **Параметры печати** в диалоговом окне " **Параметры страницы** " (на вкладке " **Конструктор** ", щелкните стрелку **Параметры страницы** ). 
  
Для получения ссылки на ячейки OnPage по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |OnPage  <br/> |
   
Для получения ссылки на ячейки OnPage по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPrintProperties** <br/> |
|Индекс ячейки:  <br/> |**visPrintPropertiesOnPage** <br/> |
   
