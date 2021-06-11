---
title: TxtLocPinX Cell (Text Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251275
localization_priority: Normal
ms.assetid: cbfc4e91-10d1-d50e-3e8a-f269f7123276
description: 'Определяет x-координату центра вращения текстового блока по отношению к происхождению текстового блока. Формула по умолчанию:'
ms.openlocfilehash: 390f8129e8000a043969eda0ab1c8e4ef62515ef
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425857"
---
# <a name="txtlocpinx-cell-text-transform-section"></a>TxtLocPinX Cell (Text Transform Section)

Определяет  x-координату центра вращения текстового блока по отношению к происхождению текстового блока. Формула по умолчанию: 
  
= TxtWidth \* 0.5
  
Эта формула оценивается в горизонтальном центре текстового блока.
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку TxtLocPinX по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | TxtLocPinX  <br/> |
   
Чтобы получить ссылку на ячейку TxtLocPinX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowTextXForm** <br/> |
| Индекс ячейки:  <br/> |**visXFormLocPinX** <br/> |
   

