---
title: UIFormat Cell (Text Fields Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1080
localization_priority: Normal
ms.assetid: 0dddef20-c58e-2306-ab8e-6cac8e159f61
description: Определяет формат вставленного поля в версиях Visio более ранних Visio 2000 г.
ms.openlocfilehash: 16cefc5f45d6b5f0f677e35bd5d0937d48fb2680
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426368"
---
# <a name="uiformat-cell-text-fields-section"></a>UIFormat Cell (Text Fields Section)

Определяет формат вставленного поля в версиях Visio более ранних Visio 2000 г.
  
## <a name="remarks"></a>Примечания

Эта ячейка не появляется в окне ShapeSheet. Используйте эту ячейку, если вам необходимо решить проблемы с обратной возможностью, например сохранить рисунок Visio версии 2000 в формате Visio версии 5.0.
  
Чтобы получить ссылку на ячейку UIFormat по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Fields.UIFmt[  *i*  ] где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку UIFormat по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionTextField** <br/> |
| Индекс строки:  <br/> |**visRowField**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
| Индекс ячейки:  <br/> |**visFieldUIFormat** <br/> |
   

