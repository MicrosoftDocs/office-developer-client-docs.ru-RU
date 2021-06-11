---
title: LineAdjustTo Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm525
localization_priority: Normal
ms.assetid: 81cd9670-8a6f-824b-528c-e9b88c86f525
description: Определяет, какие динамические соединители выстраиваются друг над другом.
ms.openlocfilehash: e4fb32c0fcb488173324ea597edc2c9d13f6bfca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414027"
---
# <a name="lineadjustto-cell-page-layout-section"></a>LineAdjustTo Cell (Page Layout Section)

Определяет, какие динамические соединители выстраиваются друг над другом.
  
|**Значение**|**Регулировка**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |По умолчанию стиль маршрутивки  <br/> |**visPLOLineAdjustToDefault** <br/> |
|1  <br/> |Строки, близкие друг к другу  <br/> |**visPLOLineAdjustToAll** <br/> |
|2  <br/> |Нет строк  <br/> |**visPLOLineAdjustToNone** <br/> |
|3  <br/> |Связанные строки  <br/> |**visPLOLineAdjustToRelated** <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить значение этой ячейки на вкладке  Layout и   **Routing** в диалоговом окне Настройка страницы (на вкладке Дизайн щелкните стрелку установки страницы, а затем нажмите макет и маршрутинг).
  
Чтобы получить ссылку на ячейку LineAdjustTo по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |LineAdjustTo  <br/> |
   
Чтобы получить ссылку на ячейку LineAdjustTo по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPageLayout** <br/> |
|Индекс ячейки:  <br/> |**visPLOLineAdjustTo** <br/> |
   

