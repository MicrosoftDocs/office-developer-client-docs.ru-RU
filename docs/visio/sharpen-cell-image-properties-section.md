---
title: Sharpen Cell (Image Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm910
localization_priority: Normal
ms.assetid: aa2bebfc-a6bb-a6b3-3ae9-8553f96b5738
description: Толстрирования тол рисунка. Значение по умолчанию — 0%. Резкое увеличение изображения фокусирует его, увеличив контрастность смежных пикселей.
ms.openlocfilehash: e519cf6e5a168b64b4bc8aa083843163a47525ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415924"
---
# <a name="sharpen-cell-image-properties-section"></a>Sharpen Cell (Image Properties Section)

Толстрирования тол рисунка. Значение по умолчанию — 0%. Резкое увеличение изображения фокусирует его, увеличив контрастность смежных пикселей.
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку Sharpen по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Sharpen  <br/> |
   
Чтобы получить ссылку на ячейку Sharpen по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowImage** <br/> |
| Индекс ячейки:  <br/> |**visImageSharpen** <br/> |
   

