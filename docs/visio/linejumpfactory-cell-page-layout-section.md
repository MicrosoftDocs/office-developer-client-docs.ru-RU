---
title: Ячейка LineJumpFactorY (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm550
localization_priority: Normal
ms.assetid: 5a14be0d-9e3c-23c4-7782-bda5470d1243
description: Определяет размер строки пересечения на вертикальной динамической соединители на странице относительно значения ячейки LineToLineY. Значение ячейки можно в диапазоне от 0 до 10, но рекомендуется дробная значения от 0 до 1.
ms.openlocfilehash: deba4c27585644604e7bac1dbfe284bc3977835e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814098"
---
# <a name="linejumpfactory-cell-page-layout-section"></a>Ячейка LineJumpFactorY (раздел "Макет страницы")

Определяет размер строки пересечения на вертикальной динамической соединители на странице относительно значения ячейки LineToLineY. Значение ячейки можно в диапазоне от 0 до 10, но рекомендуется дробная значения от 0 до 1.
  
## <a name="remarks"></a>Замечания

Значение ячейки также можно настроить на вкладке **Макет и маршрутизации** в диалоговом окне " **Параметры страницы** " (на вкладки " **Конструктор** ", нажмите кнопку со стрелкой **Параметры страницы** и нажмите кнопку **Макет и маршрутизации**).
  
Чтобы получить ссылку на ячейку LineJumpFactorY по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |LineJumpFactorY  <br/> |
   
Для получения ссылки на ячейки LineJumpFactorY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPageLayout** <br/> |
|Индекс ячейки:  <br/> |**visPLOJumpFactorY** <br/> |
   

