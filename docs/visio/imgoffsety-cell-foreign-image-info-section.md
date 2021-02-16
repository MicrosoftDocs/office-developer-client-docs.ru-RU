---
title: ImgOffsetY Cell (Foreign Image Info Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm455
localization_priority: Normal
ms.assetid: 3b2991aa-4722-fe3b-39c5-02d38c4c7efc
description: Определяет расстояние, на которое объект смещен вертикально от начала границы объекта. По умолчанию используется значение 0. Панорамирование объекта с помощью средства crop изменяет это значение.
ms.openlocfilehash: 908972216a24370bc48990ddc99a36da9274d648
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406740"
---
# <a name="imgoffsety-cell-foreign-image-info-section"></a>ImgOffsetY Cell (Foreign Image Info Section)

Определяет расстояние, на которое объект смещен вертикально от начала границы объекта. По умолчанию используется значение 0. Панорамирование объекта с помощью средства **crop** изменяет это значение. 
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку ImgOffsetY по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | ImgOffsetY  <br/> |
   
Чтобы получить ссылку на ячейку ImgOffsetY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowForeign** <br/> |
| Индекс ячейки:  <br/> |**visFrgnImgOffsetY** <br/> |
   

