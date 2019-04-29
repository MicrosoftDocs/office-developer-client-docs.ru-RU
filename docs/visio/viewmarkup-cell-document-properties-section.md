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
description: Определяет, отображаются ли разметки в окне документа.
ms.openlocfilehash: eeccdd0d14bf28630937b0e480822abb6fb19da5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416407"
---
# <a name="viewmarkup-cell-document-properties-section"></a>ViewMarkup Cell (Document Properties Section)

Определяет, отображаются ли разметки в окне документа. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |В документе отображается разМетка.  <br/> |
|FALSE  <br/> |РазМетка не отображается (значение по умолчанию).  <br/> |
   
## <a name="remarks"></a>Примечания

 Если включено отслеживание разметки (ячейка AddMarkup имеет значение TRUE), ячейка ViewMarkup автоматически задается как TRUE и остается ДЕЙСТВИТЕЛЬНОй даже после выключения отслеживания разметки (ячейка AddMarkup имеет значение FALSE). Если ячейка AddMarkup имеет значение TRUE, значение в ячейке ViewMarkup игнорируется. 
  
Ячейка ViewMarkup также имеет значение TRUE при вставке комментариев в документ (независимо от того, включено ли отслеживание разметки) и должно иметь значение TRUE, чтобы увидеть комментарии в документе.
  
Эта ячейка соответствует команде " **Показать разметку** " в группе разметки на вкладке " **Рецензирование** ". **** 
  
Чтобы получить ссылку на ячейку ViewMarkup по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |ViewMarkup  <br/> |
   
Чтобы получить ссылку на ячейку ViewMarkup по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**Висровдок** <br/> |
|Индекс ячейки:  <br/> |**Висдоквиевмаркуп** <br/> |
   

