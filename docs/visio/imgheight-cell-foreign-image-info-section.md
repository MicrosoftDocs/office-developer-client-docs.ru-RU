---
title: Ячейка ImgHeight (раздел "Сведения о внешнем изображении")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm445
localization_priority: Normal
ms.assetid: decb86a4-b711-35e1-b9dc-744a84ee177c
description: 'Определяет высоту изображения объекта в рамках его границ. Формула по умолчанию имеет вид:'
ms.openlocfilehash: 983bb919dbfada65b6d9af464ecfa17c04e970c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813951"
---
# <a name="imgheight-cell-foreign-image-info-section"></a>Ячейка ImgHeight (раздел "Сведения о внешнем изображении")

Определяет высоту изображения объекта в рамках его границ. Формула по умолчанию имеет вид:
  
= Высота \* 1
  
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку ImgHeight по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | ImgHeight  <br/> |
   
Для получения ссылки на ячейки ImgHeight по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowForeign** <br/> |
| Индекс ячейки:  <br/> |**visFrgnImgHeight** <br/> |
   

