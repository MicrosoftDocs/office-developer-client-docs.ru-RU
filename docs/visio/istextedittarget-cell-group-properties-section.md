---
title: IsTextEditTarget Cell (Group Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251627
localization_priority: Normal
ms.assetid: 355cef8b-9213-479a-af95-b591f4bc51ad
description: Определяет назначение текста для группы.
ms.openlocfilehash: 78a70dc0398745765bca12a1e768390b35fce8ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432648"
---
# <a name="istextedittarget-cell-group-properties-section"></a>IsTextEditTarget Cell (Group Properties Section)

Определяет назначение текста для группы.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Текст добавляется в фигуру группы.  <br/> |
|FALSE  <br/> |Текст добавляется к фигуре в группе в верхней части порядка размещения.  <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете задать это значение, выбрав группу, нажав кнопку **поведение** на вкладке [разработчик](run-in-developer-mode-display-the-developer-tab.md) , а затем установив флажок **изменить текст группы** . 
  
Группы, созданные в более ранних версиях, чем Visio 2000, имеют значение по умолчанию (FALSE). Начиная с Visio версии 2000, значение по умолчанию — TRUE. 
  
Чтобы получить ссылку на ячейку IsTextEditTarget по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |IsTextEditTarget  <br/> |
   
Чтобы получить ссылку на ячейку IsTextEditTarget по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**висровграуп** <br/> |
|Индекс ячейки:  <br/> |**висграупистекстедиттаржет** <br/> |
   

