---
title: PrintGrid Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033794
localization_priority: Normal
ms.assetid: 0504ff7f-2274-7ae3-1f4b-a3d890dbd79a
description: Указывает, следует ли печатать сетку при печати страницы документа.
ms.openlocfilehash: 9b98999cd02fa6a47ec8564bbd7337ecf8637306
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433208"
---
# <a name="printgrid-cell-print-properties-section"></a>PrintGrid Cell (Print Properties Section)

Указывает, следует ли печатать сетку при печати страницы документа.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Покажите сетку при печати этой страницы.  <br/> |
|FALSE  <br/> |Не показывать сетку при печати этой страницы (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Примечания

Это значение соответствует чековому окну **Gridlines** на вкладке Настройка печати в диалоговом окне Настройка страницы (на вкладке **Дизайн** щелкните стрелку **установки** страницы).   Кроме цвета (печатная версия является серой), печатная сетка идентична сетке, которая вы видите в окне рисования Microsoft Visio. 
  
Вы можете выбрать, следует ли печатать сетку на основе страницы за страницей. Стиль сетки также можно определить по странице в диалоговом окне **Линейка &amp;** Grid (на вкладке **Просмотр,** щелкните стрелку **Показать),** когда страница активна. 
  
Чтобы получить ссылку на ячейку PrintGrid по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |PrintGrid  <br/> |
   
Чтобы получить ссылку на ячейку PrintGrid по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPrintProperties** <br/> |
|Индекс ячейки:  <br/> |**visPrintPropertiesPrintGrid** <br/> |
   

