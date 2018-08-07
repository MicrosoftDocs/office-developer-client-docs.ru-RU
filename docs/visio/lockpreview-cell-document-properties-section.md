---
title: Ячейка LockPreview (раздел "Свойства документа")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251742
localization_priority: Normal
ms.assetid: 5a2bb1a7-e688-d32f-f231-ac6916d838a6
description: Определяет, сохраняется ли Предварительный просмотр каждый раз при сохранении документа.
ms.openlocfilehash: 2ef5ea12669a7a6a2b37d599afd24635f7509ac2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814142"
---
# <a name="lockpreview-cell-document-properties-section"></a>Ячейка LockPreview (раздел "Свойства документа")

Определяет, сохраняется ли Предварительный просмотр каждый раз при сохранении документа.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Не следует сохранять предварительной версии каждый раз, когда сохранения документа.  <br/> |
| FALSE  <br/> | Сохраните предварительной версии каждый раз, когда сохранения документа.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку LockPreview по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LockPreview  <br/> |
   
Для получения ссылки на ячейки LockPreview по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowDoc** <br/> |
| Индекс ячейки:  <br/> |**visDocLockPreview** <br/> |
   

