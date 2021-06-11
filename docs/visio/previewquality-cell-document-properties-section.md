---
title: PreviewQuality Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm815
localization_priority: Normal
ms.assetid: b7d90666-a1bb-f0de-32da-b2855977f648
description: Определяет, является ли предварительный просмотр эскиза качественным или подробным.
ms.openlocfilehash: 9db2d3e1eb829bfd2ad787fcfc94cd9ba5abaf9e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416820"
---
# <a name="previewquality-cell-document-properties-section"></a>PreviewQuality Cell (Document Properties Section)

Определяет, является ли предварительный просмотр эскиза качественным или подробным.
  
|**Значение**|**Качество предварительного просмотра**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Draft  <br/> |**visDocPreviewQualityDraft** <br/> |
| 1  <br/> | Подробные сведения  <br/> |**visDocPreviewQualityDetailed** <br/> |
   
## <a name="remarks"></a>Примечания

Это значение также можно задать на  вкладке **Сводка** в диалоговом окне Свойства (нажмите кнопку **Office,** нажмите вкладку **Info,** нажмите кнопку **Свойства** документа и нажмите кнопку **Расширенные свойства).**
  
Чтобы получить ссылку на ячейку PreviewQuality по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | PreviewQuality  <br/> |
   
Чтобы получить ссылку на ячейку PreviewQuality по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowDoc** <br/> |
| Индекс ячейки:  <br/> |**visDocPreviewQuality** <br/> |
   

