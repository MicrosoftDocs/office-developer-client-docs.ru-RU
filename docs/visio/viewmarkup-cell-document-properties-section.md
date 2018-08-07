---
title: Ячейка ViewMarkup (раздел "Свойства документа")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030802
localization_priority: Normal
ms.assetid: 6c956266-8266-3312-5a68-cc9d8bdb8cd9
description: Определяет, отображается ли разметка в окне документа.
ms.openlocfilehash: dda908595b243878ec755cf73351ec1fd672dc55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815157"
---
# <a name="viewmarkup-cell-document-properties-section"></a>Ячейка ViewMarkup (раздел "Свойства документа")

Определяет, отображается ли разметка в окне документа. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Разметка отображается в документе.  <br/> |
|FALSE  <br/> |Разметка не отображаются (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Замечания

 При включении отслеживания разметки (ячейки AddMarkup имеет значение TRUE), ViewMarkup ячейки автоматически устанавливается значение TRUE и остается равным TRUE даже после разметки трассировка отключена (ячейки AddMarkup — значение FALSE). Значение в ячейке ViewMarkup игнорируется, если ячейка AddMarkup имеет значение TRUE. 
  
Ячейка ViewMarkup также имеет значение TRUE, когда комментариев вставляется в документе, (ли отслеживание исправлений включено) и должно быть значение true, чтобы см. комментарии в документе.
  
В этой ячейке соответствует команда **Показать исправления** в группе **разметки** на вкладке **Обзор** . 
  
Чтобы получить ссылку на ячейку ViewMarkup по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |ViewMarkup  <br/> |
   
Для получения ссылки на ячейки ViewMarkup по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowDoc** <br/> |
|Индекс ячейки:  <br/> |**visDocViewMarkup** <br/> |
   

