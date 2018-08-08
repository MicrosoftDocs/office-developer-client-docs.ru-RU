---
title: Ячейка ImgWidth (раздел "Сведения о внешнем изображении")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm460
localization_priority: Normal
ms.assetid: b57fb962-0b3e-f2e5-3b88-3edf33e40496
description: 'Определяет ширину изображения объекта в рамках его границ. Формула по умолчанию имеет вид:'
ms.openlocfilehash: 3aab65d27d426287060f7572dad15174acb93199
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813949"
---
# <a name="imgwidth-cell-foreign-image-info-section"></a>Ячейка ImgWidth (раздел "Сведения о внешнем изображении")

Определяет ширину изображения объекта в рамках его границ. Формула по умолчанию имеет вид:
  
= Ширина \* 1
  
Обрезка объекта изменяется коэффициент, на который умножается ширина.
  
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку ImgWidth по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | ImgWidth  <br/> |
   
Для получения ссылки на ячейки ImgWidth по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowForeign** <br/> |
| Индекс ячейки:  <br/> |**visFrgnImgWidth** <br/> |
   

