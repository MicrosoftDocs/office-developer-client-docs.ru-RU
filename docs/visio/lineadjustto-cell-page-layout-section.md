---
title: Ячейка LineAdjustTo (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm525
localization_priority: Normal
ms.assetid: 81cd9670-8a6f-824b-528c-e9b88c86f525
description: Определяет, какие динамических соединители выровнять друг на друга.
ms.openlocfilehash: 13540f9dc5e6e6861d3f3679bcf49204d553397a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814078"
---
# <a name="lineadjustto-cell-page-layout-section"></a>Ячейка LineAdjustTo (раздел "Макет страницы")

Определяет, какие динамических соединители выровнять друг на друга.
  
|**Значение**|**Корректировка**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Маршрутизации по умолчанию стилей  <br/> |**visPLOLineAdjustToDefault** <br/> |
|1  <br/> |Строки, приближается к друг с другом  <br/> |**visPLOLineAdjustToAll** <br/> |
|2  <br/> |Без строк-разделителей  <br/> |**visPLOLineAdjustToNone** <br/> |
|3  <br/> |Связанные строки  <br/> |**visPLOLineAdjustToRelated** <br/> |
   
## <a name="remarks"></a>Замечания

Значение ячейки также можно настроить на вкладке **Макет и маршрутизации** в диалоговом окне " **Параметры страницы** " (на вкладки " **Конструктор** ", нажмите кнопку со стрелкой **Параметры страницы** и нажмите кнопку **Макет и маршрутизации**).
  
Чтобы получить ссылку на ячейку LineAdjustTo по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |LineAdjustTo  <br/> |
   
Для получения ссылки на ячейки LineAdjustTo по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPageLayout** <br/> |
|Индекс ячейки:  <br/> |**visPLOLineAdjustTo** <br/> |
   

