---
title: Ячейка LineRouteExt (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50115
localization_priority: Normal
ms.assetid: 3d16b8b3-601b-c10b-68a8-ffd47251306f
description: Определяет вид по умолчанию для всех соединителей на странице документа.
ms.openlocfilehash: 21da283f2d9ab43837b8fe4127840e89ea9d9949
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814101"
---
# <a name="linerouteext-cell-page-layout-section"></a>Ячейка LineRouteExt (раздел "Макет страницы")

Определяет вид по умолчанию для всех соединителей на странице документа.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | По умолчанию (обычный)  <br/> |**visLORouteExtDefault** <br/> |
| 1  <br/> | Прямой  <br/> |**visLORouteExtStraight** <br/> |
| 2  <br/> | Круглая  <br/> |**visLORouteExtNURBS** <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку LineRouteExt по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LineRouteExt  <br/> |
   
Для получения ссылки на ячейки LineRouteExt по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPageLayout** <br/> |
| Индекс ячейки:  <br/> |**visPLOLineRouteExt** <br/> |
   

