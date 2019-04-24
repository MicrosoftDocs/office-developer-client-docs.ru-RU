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
description: Определяет, сохраняется ли предварительный просмотр при каждом сохранении документа.
ms.openlocfilehash: 91362d8a88cf6db2f4807c655a6d071ebbc731f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348330"
---
# <a name="lockpreview-cell-document-properties-section"></a>LockPreview Cell (Document Properties Section)

Определяет, сохраняется ли предварительный просмотр при каждом сохранении документа.
  
|**Value**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Не сохраняйте предварительный просмотр при каждом сохранении документа.  <br/> |
| FALSE  <br/> | Сохраните предварительный просмотр при каждом сохранении документа.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку LockPreview по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LockPreview  <br/> |
   
Чтобы получить ссылку на ячейку LockPreview по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровдок** <br/> |
| Индекс ячейки:  <br/> |**Висдоклоккпревиев** <br/> |
   

