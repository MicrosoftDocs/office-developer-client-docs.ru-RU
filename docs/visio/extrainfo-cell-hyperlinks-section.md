---
title: Ячейка ExtraInfo (раздел "Гиперссылки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm360
localization_priority: Normal
ms.assetid: 55834445-8619-f79a-aea0-0f6a1780e016
description: Представляет строку, которая передает сведения, которые будут использоваться для разрешения URL-адрес, например координаты гиперкарты. Например, значение в ячейке ExtraInfo x = 41&amp;y = 7specifies координаты гиперкарты.
ms.openlocfilehash: aa035d5ec863cd8045063af970efa26b53683793
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813732"
---
# <a name="extrainfo-cell-hyperlinks-section"></a>Ячейка ExtraInfo (раздел "Гиперссылки")

Представляет строку, которая передает сведения, которые будут использоваться для разрешения URL-адрес, например координаты гиперкарты. Например, значение в ячейке ExtraInfo «x = 41&amp;y = 7» указывает координаты гиперкарты.
  
## <a name="remarks"></a>Замечания

Событие ячеек вычисляются только в том случае, когда возникает событие, не после ввода формул.
  
Для получения ссылки на ячейки ExtraInfo по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Гиперссылки.  *имя* . ExtraInfo где гиперссылки.  *имя* — это имя строки  <br/> |
   
Для получения ссылки на ячейки ExtraInfo по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionHyperlink** <br/> |
| Индекс строки:  <br/> |**visRow1stHyperlink** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visHLinkExtraInfo** <br/> |
   

