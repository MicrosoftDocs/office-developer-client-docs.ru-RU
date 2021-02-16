---
title: LockPreview Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251742
localization_priority: Normal
ms.assetid: 5a2bb1a7-e688-d32f-f231-ac6916d838a6
description: Определяет, сохраняется ли предварительный просмотр при каждом сохранения рисунка.
ms.openlocfilehash: 91362d8a88cf6db2f4807c655a6d071ebbc731f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418864"
---
# <a name="lockpreview-cell-document-properties-section"></a>LockPreview Cell (Document Properties Section)

Определяет, сохраняется ли предварительный просмотр при каждом сохранения рисунка.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Не сохранения предварительного просмотра при каждом сохранения рисунка.  <br/> |
| FALSE  <br/> | Сохранение предварительного просмотра при каждом сохранения рисунка.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку LockPreview по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LockPreview  <br/> |
   
Чтобы получить ссылку на ячейку LockPreview по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowDoc** <br/> |
| Индекс ячейки:  <br/> |**visDocLockPreview** <br/> |
   

