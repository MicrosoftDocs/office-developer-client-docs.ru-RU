---
title: Ячейка LineJumpFactorX (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm545
localization_priority: Normal
ms.assetid: 0649672f-f496-ce80-6dc3-3affc9b6f913
description: Определяет размер строки пересечения на горизонтальную динамических соединители на странице относительно значения ячейки LineToLineX. Значение ячейки можно в диапазоне от 0 до 10, но рекомендуется дробная значения от 0 до 1.
ms.openlocfilehash: fb6205407070485a0e234ee594e84979bca40891
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814074"
---
# <a name="linejumpfactorx-cell-page-layout-section"></a>Ячейка LineJumpFactorX (раздел "Макет страницы")

Определяет размер строки пересечения на горизонтальную динамических соединители на странице относительно значения ячейки LineToLineX. Значение ячейки можно в диапазоне от 0 до 10, но рекомендуется дробная значения от 0 до 1.
  
## <a name="remarks"></a>Замечания

Значение ячейки также можно настроить на вкладке **Макет и маршрутизации** в диалоговом окне " **Параметры страницы** " (на вкладки " **Конструктор** ", нажмите кнопку со стрелкой **Параметры страницы** и нажмите кнопку **Макет и маршрутизации**).
  
Чтобы получить ссылку на ячейку LineJumpFactorX по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |LineJumpFactorX  <br/> |
   
Для получения ссылки на ячейки LineJumpFactorX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPageLayout** <br/> |
|Индекс ячейки:  <br/> |**visPLOJumpFactorX** <br/> |
   
