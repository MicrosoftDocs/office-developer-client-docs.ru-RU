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
|TRUE  <br/> |Откажите сетку при печати этой страницы.  <br/> |
|FALSE  <br/> |Не показывать сетку при печати этой страницы (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Примечания

Это значение соответствует  установленного на вкладке "Настройка  печати" в диалоговом  окне "Настройка страницы" (на вкладке "Конструктор" щелкните стрелку **"Настройка** страницы").  Кроме цвета (печатная версия серая) печатная сетка идентична сетке, которая видна в окне рисования Microsoft Visio. 
  
Можно выбрать, следует ли печатать сетку по страницам. Стиль сетки также можно определить по страницам в диалоговом окне **"Линейка &amp;** сетки" (на вкладке "Вид" щелкните стрелку "Показать"), когда страница активна.   
  
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
   

