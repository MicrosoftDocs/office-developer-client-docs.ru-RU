---
title: Denoise Cell (Image Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm225
localization_priority: Normal
ms.assetid: e305585f-f0d8-0494-91d4-0c76929dc170
description: Удаляет шум (пиксели с случайно распределенными уровнями цвета) из точеченого изображения. Значение по умолчанию — 0%.
ms.openlocfilehash: f970fde22e864239ea3f3f9bcb704e7f4692e9cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415806"
---
# <a name="denoise-cell-image-properties-section"></a>Denoise Cell (Image Properties Section)

Удаляет шум (пиксели с случайно распределенными уровнями цвета) из точеченого изображения. Значение по умолчанию — 0%.
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку Denoise по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Denoise  <br/> |
   
Чтобы получить ссылку на ячейку Denoise по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowImage** <br/> |
| Индекс ячейки:  <br/> |**visImageDenoise** <br/> |
   

