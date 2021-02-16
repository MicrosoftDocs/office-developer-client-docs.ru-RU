---
title: D Cell (Connection Points Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm205
localization_priority: Normal
ms.assetid: 28b18e8d-fecf-a798-813e-c1a310002244
description: Ячейка с нуля, которую можно использовать для ввода или тестирования формул.
ms.openlocfilehash: e7bd61b8bc7a1a3b765af738681d958e2c83ba05
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408175"
---
# <a name="d-cell-connection-points-section"></a>D Cell (Connection Points Section)

Ячейка с нуля, которую можно использовать для ввода или тестирования формул.
  
## <a name="remarks"></a>Примечания

Чтобы получить доступ к ячейке D, щелкните правой кнопкой мыши строку и выберите пункт **"Изменить тип строки"** в ярлыковом меню. 
  
Чтобы получить ссылку на ячейку D по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Connections.D[  *i*  ] где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку D по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionConnectionPts** <br/> |
| Индекс строки:  <br/> |**visRowConnectionPts** +  *i*, где *i* = 0, 1, 2…  <br/> |
| Индекс ячейки:  <br/> |**visCnnctD** <br/> |
   

