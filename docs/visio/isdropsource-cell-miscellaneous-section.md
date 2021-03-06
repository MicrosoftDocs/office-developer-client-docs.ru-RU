---
title: IsDropSource Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm490
localization_priority: Normal
ms.assetid: 3b20e6ef-f1ac-5bb0-5ac3-4df3ae5e9bf9
description: Определяет, можно ли добавить фигуру в группу, сбросив ее в группу.
ms.openlocfilehash: e8cb02a66f745530f12c7c8be56b9bdd771121b7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421895"
---
# <a name="isdropsource-cell-miscellaneous-section"></a>IsDropSource Cell (Miscellaneous Section)

Определяет, можно ли добавить фигуру в группу, сбросив ее в группу.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Можно добавить фигуру в группу, сбросив ее в группу.  <br/> |
|FALSE  <br/> |Не удается добавить фигуру в группу.  <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить это значение, выбрав  фигуру, щелкнув "Поведение" на вкладке Разработчик, а затем выбрав фигуру **Добавить** к группам на drop check box. [](run-in-developer-mode-display-the-developer-tab.md) 
  
Помимо включения этого поведения для фигуры, необходимо также включить группу для того, чтобы принимать фигуры, которые в нее втянуты. Для этого выберите группу, щелкните **"Поведение"** на вкладке ["Разработчик",](run-in-developer-mode-display-the-developer-tab.md) а затем выберите поле **"Принять выброшенные** фигуры". Это значение хранится в ячейке IsDropTarget в разделе Group Properties. 
  
Чтобы получить ссылку на ячейку IsDropSource по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |IsDropSource  <br/> |
   
Чтобы получить ссылку на ячейку IsDropSource по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowMisc** <br/> |
|Индекс ячейки:  <br/> |**visDropSource** <br/> |
   

