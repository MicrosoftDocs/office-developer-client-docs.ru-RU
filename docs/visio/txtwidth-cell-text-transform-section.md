---
title: TxtWidth Cell (Text Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251270
localization_priority: Normal
ms.assetid: e2215c67-25fa-1d75-9cce-f126bb8760a1
description: 'Определяет ширину текстового блока. Формула по умолчанию:'
ms.openlocfilehash: 806307166035ebc2f8e20e7025d5ecb03c4d6e79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426095"
---
# <a name="txtwidth-cell-text-transform-section"></a>TxtWidth Cell (Text Transform Section)

Определяет ширину текстового блока. Формула по умолчанию:
  
= Ширина \* 1
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку TxtWidth по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | TxtWidth  <br/> |
   
Чтобы получить ссылку на ячейку TxtWidth по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowTextXForm** <br/> |
| Индекс ячейки:  <br/> |**visXFormWidth** <br/> |
   

