---
title: ImgHeight Cell (Foreign Image Info Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm445
localization_priority: Normal
ms.assetid: decb86a4-b711-35e1-b9dc-744a84ee177c
description: 'Определяет высоту изображения объекта в пределах его границ. По умолчанию используется следующая формула:'
ms.openlocfilehash: 956bc478604fd19d8dfdbb7079e092e9e8a16e7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344935"
---
# <a name="imgheight-cell-foreign-image-info-section"></a>ImgHeight Cell (Foreign Image Info Section)

Определяет высоту изображения объекта в пределах его границ. По умолчанию используется следующая формула:
  
= Высота \* 1
  
## <a name="remarks"></a>Комментарии

Чтобы получить ссылку на ячейку ImgHeight по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | ImgHeight  <br/> |
   
Чтобы получить ссылку на ячейку ImgHeight по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровфореигн** <br/> |
| Индекс ячейки:  <br/> |**Висфргнимгхеигхт** <br/> |
   

