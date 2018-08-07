---
title: Ячейка LineAdjustFrom (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251887
localization_priority: Normal
ms.assetid: 6949c717-dc69-1d17-5215-eb6efce56fcb
description: Определяет, какие динамических соединители пробелы приложения друг от друга, если они маршрутизировать друг на друга.
ms.openlocfilehash: ee3a107f7e19b53017c2ea24c94babceb49620d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814067"
---
# <a name="lineadjustfrom-cell-page-layout-section"></a>Ячейка LineAdjustFrom (раздел "Макет страницы")

Определяет, какие динамических соединители пробелы приложения друг от друга, если они маршрутизировать друг на друга.
  
|**Значение**|**Корректировка**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Несвязанные линии  <br/> |**visPLOLineAdjustFromNotRelated** <br/> |
|1  <br/> |Все строки  <br/> |**visPLOLineAdjustFromAll** <br/> |
|2  <br/> |Без строк-разделителей  <br/> |**visPLOLineAdjustFromNone** <br/> |
|3  <br/> |Маршрутизации по умолчанию стилей  <br/> |**visPLOLineAdjustFromRoutingDefault** <br/> |
   
## <a name="remarks"></a>Замечания

Значение ячейки также можно настроить на вкладке **Макет и маршрутизации** в диалоговом окне " **Параметры страницы** " (на вкладки " **Конструктор** ", нажмите кнопку со стрелкой **Параметры страницы** и нажмите кнопку **Макет и маршрутизации**).
  
Чтобы получить ссылку на ячейку LineAdjustFrom по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |LineAdjustFrom  <br/> |
   
Для получения ссылки на ячейки LineAdjustFrom по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPageLayout** <br/> |
|Индекс ячейки:  <br/> |**visPLOLineAdjustFrom** <br/> |
   

