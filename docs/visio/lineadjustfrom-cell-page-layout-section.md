---
title: LineAdjustFrom Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251887
localization_priority: Normal
ms.assetid: 6949c717-dc69-1d17-5215-eb6efce56fcb
description: Определяет, какие динамические соединители пространство приложения друг от друга, если они следования друг на друга.
ms.openlocfilehash: 3eb9f5513ee3ce2f5dce96cb47c356bca29a289c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415189"
---
# <a name="lineadjustfrom-cell-page-layout-section"></a>LineAdjustFrom Cell (Page Layout Section)

Определяет, какие динамические соединители пространство приложения друг от друга, если они следования друг на друга.
  
|**Значение**|**Регулировка**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Несвязанные строки  <br/> |**visPLOLineAdjustFromNotRelated** <br/> |
|1  <br/> |Все строки  <br/> |**visPLOLineAdjustFromAll** <br/> |
|2  <br/> |Нет строк  <br/> |**visPLOLineAdjustFromNone** <br/> |
|3  <br/> |По умолчанию стиль маршрутивки  <br/> |**visPLOLineAdjustFromRoutingDefault** <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить значение этой ячейки на вкладке  Layout и   **Routing** в диалоговом окне Настройка страницы (на вкладке Дизайн щелкните стрелку установки страницы, а затем нажмите макет и маршрутинг).
  
Чтобы получить ссылку на ячейку LineAdjustFrom по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |LineAdjustFrom  <br/> |
   
Чтобы получить ссылку на ячейку LineAdjustFrom по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPageLayout** <br/> |
|Индекс ячейки:  <br/> |**visPLOLineAdjustFrom** <br/> |
   

