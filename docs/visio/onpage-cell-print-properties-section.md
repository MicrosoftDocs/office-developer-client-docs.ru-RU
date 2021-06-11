---
title: OnPage Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033793
localization_priority: Normal
ms.assetid: 4015506a-e24a-0276-c854-7791a7019067
description: Указывает, напечатан ли рисунок на определенном количестве страниц принтера.
ms.openlocfilehash: 61d45a5bffdbb1afd5db9c608f80bc4f797f5191
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439606"
---
# <a name="onpage-cell-print-properties-section"></a>OnPage Cell (Print Properties Section)

Указывает, напечатан ли рисунок на определенном количестве страниц принтера. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Примыкать страницу рисования к определенному числу страниц принтера.  <br/> |
|FALSE  <br/> |Не подходит страница рисования к определенному числу страниц принтера (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Примечания

Если ячейка OnPage настроена на TRUE, microsoft Visio использует ячейки PagesX и PagesY для определения количества страниц принтера, на которых должен соответствовать рисунок. Значения в ячейках ScaleX и ScaleY игнорируются. Это можно считать параметром автомасштаба.
  
Это значение соответствует параметру Fit  **для** параметра на вкладке Настройка печати в диалоговом окне **Настройка** страницы (на вкладке **Дизайн** щелкните стрелку **установки** страницы) . 
  
Чтобы получить ссылку на ячейку OnPage по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |OnPage  <br/> |
   
Чтобы получить ссылку на ячейку OnPage по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPrintProperties** <br/> |
|Индекс ячейки:  <br/> |**visPrintPropertiesOnPage** <br/> |
   

