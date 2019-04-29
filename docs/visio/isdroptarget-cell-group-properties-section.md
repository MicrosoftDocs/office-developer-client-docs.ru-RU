---
title: IsDropTarget Cell (Group Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm495
localization_priority: Normal
ms.assetid: 8140fc7b-b99c-54bb-7af3-7de6fcdae7d3
description: Определяет, можно ли добавить фигуру в группу, перетащив ее в группу.
ms.openlocfilehash: 50f545b3cbd4f7e1541a7f5e8ca32c34d0429c5e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410793"
---
# <a name="isdroptarget-cell-group-properties-section"></a>IsDropTarget Cell (Group Properties Section)

Определяет, можно ли добавить фигуру в группу, перетащив ее в группу.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Можно добавить фигуру в группу, перетащив ее в группу.  <br/> |
|FALSE  <br/> |Не удается удалить фигуру в группу.  <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете задать это значение, выбрав группу, нажав кнопку **поведение** на вкладке [разработчик](run-in-developer-mode-display-the-developer-tab.md) и установив флажок **принять пропущенные фигуры** . 
  
Чтобы добавить фигуру в группу, перетащите ее в группу, необходимо также включить схожее поведение фигуры. Необходимо выбрать фигуру, нажать кнопку **поведение** на вкладке [разработчик](run-in-developer-mode-display-the-developer-tab.md) , а затем установить флажок **Добавить фигуру в группы при удалении** . Это значение хранится в ячейке IsDropSource в разделе Разное. 
  
Чтобы получить ссылку на ячейку IsDropTarget по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |IsDropTarget  <br/> |
   
Чтобы получить ссылку на ячейку IsDropTarget по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**Висровграуп** <br/> |
|Индекс ячейки:  <br/> |**Висграуписдроптаржет** <br/> |
   

