---
title: Ячейка LineJumpStyle (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251646
localization_priority: Normal
ms.assetid: 89f16674-ee1f-f5f9-9830-7bcc52e3a068
description: Определяет стиль значка для всех соединителей на странице документа, не имеющих локальных стиль перехода.
ms.openlocfilehash: 96941f675b67b38a8575bd712db5ad0eb76cd50f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814088"
---
# <a name="linejumpstyle-cell-page-layout-section"></a>Ячейка LineJumpStyle (раздел "Макет страницы")

Определяет стиль значка для всех соединителей на странице документа, не имеющих локальных стиль перехода.
  
|**Значение**|**Линии началу работы**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |ARC  <br/> |**visLOJumpStyleDefault** <br/> |
|1  <br/> |ARC  <br/> |**visLOJumpStyleArc** <br/> |
|2  <br/> |Разрывов  <br/> |**visLOJumpStyleGap** <br/> |
|3  <br/> |Квадратный  <br/> |**visLOJumpStyleSquare** <br/> |
|4  <br/> |Двусторонняя  <br/> |**visLOJumpStyleTriangle** <br/> |
|5  <br/> |три стороны  <br/> |**visLOJumpStyle2Point** <br/> |
|6  <br/> |4 сторон  <br/> |**visLOJumpStyle3Point** <br/> |
|7  <br/> |5 сторон  <br/> |**visLOJumpStyle4Point** <br/> |
|8  <br/> |6 сторон  <br/> |**visLOJumpStyle5Point** <br/> |
|9  <br/> |7 сторон  <br/> |**visLOJumpStyle6Point** <br/> |
   
## <a name="remarks"></a>Замечания

Значение ячейки также можно настроить на вкладке **Макет и маршрутизации** в диалоговом окне " **Параметры страницы** " (на вкладки " **Конструктор** ", нажмите кнопку со стрелкой **Параметры страницы** и нажмите кнопку **Макет и маршрутизации**).
  
Чтобы получить ссылку на ячейку LineJumpStyle по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |LineJumpStyle  <br/> |
   
Для получения ссылки на ячейки LineJumpStyle по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPageLayout** <br/> |
|Индекс ячейки:  <br/> |**visPLOJumpStyle** <br/> |
   

