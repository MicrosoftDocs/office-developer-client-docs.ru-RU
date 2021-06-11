---
title: LineCap Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251231
localization_priority: Normal
ms.assetid: 3519216b-b6cf-2e8c-e20f-adfa373c9028
description: Указывает, закруглили ли строки, квадрат или расширенные ограничения строки.
ms.openlocfilehash: 44de4bff87fd3d121dfce9eec934ec39bc61065a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425201"
---
# <a name="linecap-cell-line-format-section"></a>LineCap Cell (Line Format Section)

Указывает, закруглили ли строки, квадрат или расширенные ограничения строки.
  
|**Значение**|**Стиль конца строки**|
|:-----|:-----|
|0  <br/> |Округлый  <br/> |
|1  <br/> |Square  <br/> |
|2  <br/> |Долго  <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить значение этой ячейки в диалоговом окне **Line** (на вкладке Главная, в группе **Shape** щелкните Строка, указать стрелки, а затем нажмите кнопку **Дополнительные стрелки).**   
  
Чтобы получить ссылку на ячейку LineCap по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |LineCap  <br/> |
   
Чтобы получить ссылку на ячейку LineCap по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowLine** <br/> |
|Индекс ячейки:  <br/> |**visLineEndCap** <br/> |
   

