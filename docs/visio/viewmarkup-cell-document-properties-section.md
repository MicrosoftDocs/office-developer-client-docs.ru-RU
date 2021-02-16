---
title: ViewMarkup Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030802
localization_priority: Normal
ms.assetid: 6c956266-8266-3312-5a68-cc9d8bdb8cd9
description: Определяет, отображается ли разметка в окне рисования.
ms.openlocfilehash: eeccdd0d14bf28630937b0e480822abb6fb19da5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416407"
---
# <a name="viewmarkup-cell-document-properties-section"></a>ViewMarkup Cell (Document Properties Section)

Определяет, отображается ли разметка в окне рисования. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Разметка отображается на рисунке.  <br/> |
|FALSE  <br/> |Разметка не отображается (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Примечания

 Если отслеживание разметки включено (ячейка AddMarkup имеет true), ячейка ViewMarkup автоматически получает true и остается TRUE даже после отключения отслеживания разметки (ячейка AddMarkup имеет вид FALSE). Значение в ячейке ViewMarkup игнорируется, если ячейка AddMarkup имеет значение TRUE. 
  
Ячейка ViewMarkup также имеет true, когда комментарии вставляются в рисунок (включено ли отслеживание разметки) и должна иметь true, чтобы увидеть комментарии в рисунке.
  
Эта ячейка соответствует команде **"Показать разметку"** в группе **разметки** на вкладке **"Обзор".** 
  
Чтобы получить ссылку на ячейку ViewMarkup по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |ViewMarkup  <br/> |
   
Чтобы получить ссылку на ячейку ViewMarkup по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowDoc** <br/> |
|Индекс ячейки:  <br/> |**visDocViewMarkup** <br/> |
   

