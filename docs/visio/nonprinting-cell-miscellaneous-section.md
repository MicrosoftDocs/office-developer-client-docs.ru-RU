---
title: NonPrinting Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251321
localization_priority: Normal
ms.assetid: 59fe0887-2092-4fad-ea38-2aba354f3b92
description: Включает и выключает печать для выбранной фигуры.
ms.openlocfilehash: c3e1fc1b2d91fa4808f8ea89c904218c2236f5b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437261"
---
# <a name="nonprinting-cell-miscellaneous-section"></a>NonPrinting Cell (Miscellaneous Section)

Включает и выключает печать для выбранной фигуры.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Печать отключена, но фигура будет отображаться в окне документа.  <br/> |
| FALSE  <br/> | Печать включена.  <br/> |
   
## <a name="remarks"></a>Примечания

Вы можете напечатать направляющую, выбрав ее, а затем присвоив непечатаемой ячейке значение FALSE.
  
Чтобы получить ссылку на непечатаемую ячейку по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | NonPrinting  <br/> |
   
Чтобы получить ссылку на непечатаемую ячейку по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**висровмиск** <br/> |
| Индекс ячейки:  <br/> |**виснонпринтинг** <br/> |
   

