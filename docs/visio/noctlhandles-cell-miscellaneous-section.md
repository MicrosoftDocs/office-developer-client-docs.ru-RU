---
title: NoCtlHandles Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251319
localization_priority: Normal
ms.assetid: 4345b3e5-f522-e300-307c-4f8992a3ddce
description: Переключает отображение десков управления для выбранной фигуры.
ms.openlocfilehash: cbe4d6a8b6fdd4b66acf064884d20999ff7e3b4f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416127"
---
# <a name="noctlhandles-cell-miscellaneous-section"></a>NoCtlHandles Cell (Miscellaneous Section)

Переключает отображение десков управления для выбранной фигуры.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Handles control are not displayed when a shape is selected.  <br/> |
| FALSE  <br/> | Handles control are displayed when a shape is selected.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку NoCtlHandles по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | NoCtlHandles  <br/> |
   
Чтобы получить ссылку на ячейку NoCtlHandles по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowMisc** <br/> |
| Индекс ячейки:  <br/> |**visNoCtlHandles** <br/> |
   

