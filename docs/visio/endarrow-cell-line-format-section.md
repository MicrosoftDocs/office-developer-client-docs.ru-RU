---
title: EndArrow Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm320
localization_priority: Normal
ms.assetid: 2f9c11ba-a316-bc34-60d4-0a41b2af486f
description: Указывает, имеет ли строка стрелку или другой конечный формат строки на последнем вершине.
ms.openlocfilehash: 54ef11125a8774914a60897850fb75cd4ab949a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434685"
---
# <a name="endarrow-cell-line-format-section"></a>EndArrow Cell (Line Format Section)

Указывает, имеет ли строка стрелку или другой конечный формат строки на последнем вершине.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Без наконечника стрелы.  <br/> |
|1 - 45  <br/> |Различные стили наконечники стрел, соответствующие индексным записям в диалоговом окне **Line.**  <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить это значение в диалоговом окне **Line** (на вкладке **Главная,** в группе **Shape** нажмите кнопку **Line,** указать стрелки, а затем нажмите кнопку **Дополнительные стрелки).** Размер наконечника стрелки устанавливается в ячейке EndArrowSize.
  
Вы можете указать настраиваемый конец строки с помощью функции USE в этой ячейке. 
  
Чтобы получить ссылку на ячейку EndArrow по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |EndArrow  <br/> |
   
Чтобы получить ссылку на ячейку EndArrow по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowLine** <br/> |
|Индекс ячейки:  <br/> |**visLineEndArrow** <br/> |
   

