---
title: UICode Cell (Text Fields Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1075
localization_priority: Normal
ms.assetid: 1d9717c1-4310-0d62-874f-4df77cd81627
description: Определяет код вставленного поля в версиях Visio более чем Visio 2000 г.
ms.openlocfilehash: 293451b61def59ccfdf849dc597def9521fd22e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422217"
---
# <a name="uicode-cell-text-fields-section"></a>UICode Cell (Text Fields Section)

Определяет код вставленного поля в версиях Visio более чем Visio 2000 г.
  
## <a name="remarks"></a>Примечания

Эта ячейка не появляется в окне ShapeSheet. Используйте эту ячейку, если вам необходимо решить проблемы с обратной возможностью, например сохранить рисунок Visio версии 2000 в формате Visio версии 5.0.
  
Чтобы получить ссылку на ячейку UICode по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Fields.UICod[  *i*  ] где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку UICode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionTextField** <br/> |
| Индекс строки:  <br/> |**visRowField**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
| Индекс ячейки:  <br/> |**visFieldUICode** <br/> |
   

