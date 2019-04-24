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
description: Определяет, является ли предварительный просмотр изображения черновым или подробным.
ms.openlocfilehash: 9db2d3e1eb829bfd2ad787fcfc94cd9ba5abaf9e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356037"
---
# <a name="previewquality-cell-document-properties-section"></a>PreviewQuality Cell (Document Properties Section)

Определяет, является ли предварительный просмотр изображения черновым или подробным.
  
|**Значение**|**Предварительное качество**|**Константа автоматизации**|
|:-----|:-----|:-----|
| нуль  <br/> | Черновик  <br/> |**Висдокпревиевкуалитидрафт** <br/> |
| 1,1  <br/> | Дроб  <br/> |**Висдокпревиевкуалитидетаилед** <br/> |
   
## <a name="remarks"></a>Примечания

Это значение можно также задать на вкладке **Сводка** диалогового окна **Свойства** (нажмите кнопку **Office** , перейдите на вкладку **сведения** , щелкните **Свойства документа**, а затем выберите **Дополнительные свойства**).
  
Чтобы получить ссылку на ячейку PreviewQuality по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | PreviewQuality  <br/> |
   
Чтобы получить ссылку на ячейку PreviewQuality по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровдок** <br/> |
| Индекс ячейки:  <br/> |**Висдокпревиевкуалити** <br/> |
   

