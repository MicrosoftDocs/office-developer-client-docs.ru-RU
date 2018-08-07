---
title: Ячейка InhibitSnap (раздел "Свойства страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251620
localization_priority: Normal
ms.assetid: ab9fcebc-1550-3b9e-e3b4-e8b92424390b
description: Определяет, будет ли фигуры на переднем плане привязать к другие объекты на странице и фигуры на странице заднего плана.
ms.openlocfilehash: b95dafda9ebef36db34f60585ab3ed2164ade415
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813962"
---
# <a name="inhibitsnap-cell-page-properties-section"></a>Ячейка InhibitSnap (раздел "Свойства страницы")

Определяет, будет ли фигуры на переднем плане привязать к другие объекты на странице и фигуры на странице заднего плана.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Запретить все привязки на странице, за исключением привязка к линейки и сетки.  <br/> |
| FALSE  <br/> | Включение привязки.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку InhibitSnap по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | InhibitSnap  <br/> |
   
Для получения ссылки на ячейки InhibitSnap по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPage** <br/> |
| Индекс ячейки:  <br/> |**visPageInhibitSnap** <br/> |
   

