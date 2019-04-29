---
title: ImgWidth Cell (Foreign Image Info Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm460
localization_priority: Normal
ms.assetid: b57fb962-0b3e-f2e5-3b88-3edf33e40496
description: 'Определяет ширину изображения объекта в пределах его границ. По умолчанию используется следующая формула:'
ms.openlocfilehash: 9da5e06a7fbf6ae77a49fb0410aefb406e2afecb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422833"
---
# <a name="imgwidth-cell-foreign-image-info-section"></a>ImgWidth Cell (Foreign Image Info Section)

Определяет ширину изображения объекта в пределах его границ. По умолчанию используется следующая формула:
  
= Width \* 1
  
При кадрировании объекта изменяется коэффициент, на который умножается ширина.
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку ImgWidth по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | ImgWidth  <br/> |
   
Чтобы получить ссылку на ячейку ImgWidth по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровфореигн** <br/> |
| Индекс ячейки:  <br/> |**Висфргнимгвидс** <br/> |
   

