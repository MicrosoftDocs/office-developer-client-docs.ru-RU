---
title: Contrast Cell (Image Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm200
localization_priority: Normal
ms.assetid: f0e4c644-c646-9649-c697-82feb02f5e29
description: Регулирует контраст изображения bitmap. Уменьшите контраст изображения, введите значение от 0% до 49%, или увеличив контраст, введите значение от 51% до 100%. Значение по умолчанию — 50%.
ms.openlocfilehash: f0a27090ea1ec96bf11726ae641ff918dd581e2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404927"
---
# <a name="contrast-cell-image-properties-section"></a>Contrast Cell (Image Properties Section)

Регулирует контраст изображения bitmap. Уменьшите контраст изображения, введите значение от 0% до 49%, или увеличив контраст, введите значение от 51% до 100%. Значение по умолчанию — 50%.
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку Contrast по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Контраст  <br/> |
   
Чтобы получить ссылку на ячейку Contrast по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowImage** <br/> |
| Индекс ячейки:  <br/> |**visImageContrast** <br/> |
   

