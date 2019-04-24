---
title: LangID Cell (Annotation Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60048
localization_priority: Normal
ms.assetid: b6f5ea5e-b350-0817-d631-f059b9b95c23
description: Указывает язык, на котором был введен комментарий.
ms.openlocfilehash: b3b2cba3d0a04f75ef2d87f0ee8dcd1f8115e15e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360552"
---
# <a name="langid-cell-annotation-section"></a>LangID Cell (Annotation Section)

Указывает язык, на котором был введен комментарий.
  
> [!NOTE]
> Эта ячейка используется для отслеживания комментариев только при открытии VSD-файла в Microsoft Visio 2013 или при сохранении VSDX-файла в формате VSD-файла. Она не используется для отслеживания комментариев в VSDX-документах в Visio 2013. 
  
## <a name="remarks"></a>Замечания

Это значение представляет собой код языка (LCID), который активен на языковой панели при вводе комментария. Список языков, поддерживаемых приложениями Microsoft Office, приведен в разделе [DocLangID](doclangid-cell-document-properties-section.md) Cell (раздел "Свойства документа"). 
  
Чтобы получить ссылку на ячейку LangID по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Аннотация. LangID [ *i* ], где *i* = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку LangID по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionAnnotation** <br/> |
| Индекс строки:  <br/> |**visRowAnnotation** +  *i*, где *i* = 0, 1, 2…  <br/> |
| Индекс ячейки:  <br/> |**Висаннотатионлангид** <br/> |
   

