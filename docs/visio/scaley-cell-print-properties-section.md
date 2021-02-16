---
title: ScaleY Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033788
localization_priority: Normal
ms.assetid: 02835aff-455b-ffeb-d53b-28387b6ce361
description: Указывает процент увеличения страницы рисования на странице принтера.
ms.openlocfilehash: 0f8e86675a039002b60438eac7df92f4a2b13b98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406992"
---
# <a name="scaley-cell-print-properties-section"></a>ScaleY Cell (Print Properties Section)

Указывает процент увеличения страницы рисования на странице принтера.
  
## <a name="remarks"></a>Примечания

Это значение используется, только если значение ячейки OnPage — FALSE. Ячейки ScaleX и ScaleY всегда имеют одно и то же значение,  соответствующее значению  в параметре **"Настройка"** на вкладке "Настройка печати" в диалоговом окне "Настройка страницы" (на вкладке "Конструктор" щелкните стрелку "Настройка страницы").   
  
Чтобы получить ссылку на ячейку ScaleY по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |ScaleY  <br/> |
   
Чтобы получить ссылку на ячейку ScaleY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPrintProperties** <br/> |
|Индекс ячейки:  <br/> |**visPrintPropertiesScaleY** <br/> |
   

