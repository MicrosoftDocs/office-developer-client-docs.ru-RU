---
title: DrawingSizeType Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm275
localization_priority: Normal
ms.assetid: 7fe270e8-0dff-bf1f-dfc0-c0608af79f59
description: Определяет размер рисунка.
ms.openlocfilehash: 33c85b6c2f0587654038eaec1a9490ca8bd8301b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425451"
---
# <a name="drawingsizetype-cell-page-properties-section"></a>DrawingSizeType Cell (Page Properties Section)

Определяет размер рисунка.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |То же, что и принтер  <br/> |**visPrintSetup** <br/> |
|1   <br/> |Подгонка страницы к содержимому  <br/> |**visTight** <br/> |
|2   <br/> |Стандартный  <br/> |**visStandard** <br/> |
|3   <br/> |Пользовательский размер страницы  <br/> |**visCustom** <br/> |
|4   <br/> |Пользовательский масштабный размер рисунка  <br/> |**visLogical** <br/> |
|5   <br/> |Метрика (ISO)  <br/> |**visDSMetric** <br/> |
|6   <br/> |ANSI Engineering  <br/> |**visDSEngr** <br/> |
|7   <br/> |Архитектура ANSI  <br/> |**visDSArch** <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы установить размер рисунка, используйте диалоговое окно  "Настройка страницы" (щелкните стрелку "Настройка страницы" на вкладке "Конструктор") или вручную измерите размер страницы мышью.   
  
Чтобы получить ссылку на ячейку DrawingSizeType по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |DrawingSizeType  <br/> |
   
Чтобы получить ссылку на ячейку DrawingSizeType по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPage** <br/> |
|Индекс ячейки:  <br/> |**visPageDrawSizeType** <br/> |
   

