---
title: TxtPinX Cell (Text Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1040
localization_priority: Normal
ms.assetid: d0c0fe52-6a9e-e40e-394e-83a851db55a4
description: 'Определяет x-координату центра вращения текстового блока относительно начала фигуры. Формула по умолчанию:'
ms.openlocfilehash: 836f5c807d0c0e53efc825f62f60429274282165
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423498"
---
# <a name="txtpinx-cell-text-transform-section"></a>TxtPinX Cell (Text Transform Section)

Определяет  *x-координату*  центра вращения текстового блока относительно начала фигуры. Формула по умолчанию: 
  
= \* Ширина 0,5
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку TxtPinX по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | TxtPinX  <br/> |
   
Чтобы получить ссылку на ячейку TxtPinX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowTextXForm** <br/> |
| Индекс ячейки:  <br/> |**visXFormPinX** <br/> |
   

