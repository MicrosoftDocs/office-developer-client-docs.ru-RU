---
title: Ячейка PreviewQuality (раздел "Свойства документа")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm815
localization_priority: Normal
ms.assetid: b7d90666-a1bb-f0de-32da-b2855977f648
description: Определяет, является ли образца документа черновиков качество или подробное.
ms.openlocfilehash: bc8a53934b6dad06a0867cc73cdfacfa02d2b438
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814461"
---
# <a name="previewquality-cell-document-properties-section"></a>Ячейка PreviewQuality (раздел "Свойства документа")

Определяет, является ли образца документа черновиков качество или подробное.
  
|**Значение**|**Качество предварительного просмотра**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Черновик  <br/> |**visDocPreviewQualityDraft** <br/> |
| 1  <br/> | Detailed  <br/> |**visDocPreviewQualityDetailed** <br/> |
   
## <a name="remarks"></a>Замечания

Это значение также можно настроить на вкладке **Обзор** в диалоговом окне **Свойства** (нажмите кнопку **Office** , перейдите на вкладку **сведения** , нажмите кнопку **Свойства документа**и выберите команду **Дополнительные свойства**).
  
Чтобы получить ссылку на ячейку PreviewQuality по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | PreviewQuality  <br/> |
   
Для получения ссылки на ячейки PreviewQuality по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowDoc** <br/> |
| Индекс ячейки:  <br/> |**visDocPreviewQuality** <br/> |
   

