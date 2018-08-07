---
title: Ячейка ScaleX (раздел "Свойства печати")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60072
localization_priority: Normal
ms.assetid: 5916eadc-37f8-47af-fe54-f6062aea318f
description: Указывает процент увеличения страницы документа на странице принтера.
ms.openlocfilehash: 1713e88f06dc93a2806e64cae3d7af20c9df1fc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814728"
---
# <a name="scalex-cell-print-properties-section"></a>Ячейка ScaleX (раздел "Свойства печати")

Указывает процент увеличения страницы документа на странице принтера.
  
## <a name="remarks"></a>Замечания

Это значение используется только в том случае, если значение ячейки OnPage — FALSE. Ячейки ScaleX и ScaleY всегда с таким же значением, который соответствует значению в параметре **обеспечить, чтобы** на вкладке **Параметры печати** в диалоговом окне " **Параметры страницы** " (на вкладке " **Конструктор** ", щелкните стрелку **Параметры страницы** ). 
  
Чтобы получить ссылку на ячейку ScaleX по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |ScaleX  <br/> |
   
Для получения ссылки на ячейки ScaleX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPrintProperties** <br/> |
|Индекс ячейки:  <br/> |**visPrintPropertiesScaleX** <br/> |
   

