---
title: ExtraInfo Cell (Hyperlinks Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm360
localization_priority: Normal
ms.assetid: 55834445-8619-f79a-aea0-0f6a1780e016
description: Представляет строку, которая передает сведения, которые будут использоваться для решения URL-адреса, например координаты карты изображений. Например, в ячейке ExtraInfo x=41 &amp; y=7specifies передает координаты карты изображений.
ms.openlocfilehash: df2886ef7911b484cc60e8a476bfa53369fbf646
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409575"
---
# <a name="extrainfo-cell-hyperlinks-section"></a>ExtraInfo Cell (Hyperlinks Section)

Представляет строку, которая передает сведения, которые будут использоваться для решения URL-адреса, например координаты карты изображений. Например, в ячейке ExtraInfo "x=41 &amp; y=7" указывает координаты карты изображений.
  
## <a name="remarks"></a>Примечания

Ячейки событий оцениваются только при событии, а не при входе формулы.
  
Чтобы получить ссылку на ячейку ExtraInfo по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Гиперссылка.  *имя*  . ExtraInfo, где гиперссылка.  *имя*  — это имя строки  <br/> |
   
Чтобы получить ссылку на ячейку ExtraInfo по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionHyperlink** <br/> |
| Индекс строки:  <br/> |**visRow1stHyperlink**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
| Индекс ячейки:  <br/> |**visHLinkExtraInfo** <br/> |
   

