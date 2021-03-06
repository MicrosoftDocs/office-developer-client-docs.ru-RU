---
title: ImgOffsetX Cell (Foreign Image Info Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251308
localization_priority: Normal
ms.assetid: c079fb10-4db7-4657-75d2-2fb953c86670
description: Определяет расстояние, на которое объект смещен горизонтально от начала границы объекта. По умолчанию используется значение 0. Панорамирование объекта с помощью средства Crop изменяет это значение.
ms.openlocfilehash: d9b3e97a07bc1cadc0276905c4199861ab0590ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405235"
---
# <a name="imgoffsetx-cell-foreign-image-info-section"></a>ImgOffsetX Cell (Foreign Image Info Section)

Определяет расстояние, на которое объект смещен горизонтально от начала границы объекта. По умолчанию используется значение 0. Панорамирование объекта с помощью средства **Crop** изменяет это значение. 
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку ImgOffsetX по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | ImgOffsetX  <br/> |
   
Чтобы получить ссылку на ячейку ImgOffsetX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowForeign** <br/> |
| Индекс ячейки:  <br/> |**visFrgnImgOffsetX** <br/> |
   

