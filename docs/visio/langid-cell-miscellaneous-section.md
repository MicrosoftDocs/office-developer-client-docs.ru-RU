---
title: LangID Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60051
localization_priority: Normal
ms.assetid: 815e0df8-5ebf-ef1b-d620-bce8abb69f1a
description: Указывает язык, на котором были созданы формулы ячеек.
ms.openlocfilehash: e1e5b92f01e97bc63003a4b195c159a50f61e77b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406677"
---
# <a name="langid-cell-miscellaneous-section"></a>LangID Cell (Miscellaneous Section)

Указывает язык, на котором были созданы формулы ячеек. 
  
## <a name="remarks"></a>Примечания

Список языков, поддерживаемых приложениями Microsoft Office, приведен в разделе [DocLangID](doclangid-cell-document-properties-section.md) Cell (раздел "Свойства документа"). 
  
Чтобы получить ссылку на ячейку LangID по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LangID  <br/> |
   
Чтобы получить ссылку на ячейку LangID по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**висровмиск** <br/> |
| Индекс ячейки:  <br/> |**висобжлангид** <br/> |
   

