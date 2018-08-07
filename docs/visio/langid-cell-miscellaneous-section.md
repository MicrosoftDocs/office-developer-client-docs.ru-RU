---
title: Ячейка LangID (раздел "Прочее")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60051
localization_priority: Normal
ms.assetid: 815e0df8-5ebf-ef1b-d620-bce8abb69f1a
description: Указывает язык, на какие ячейки были созданы формулы.
ms.openlocfilehash: 669bde032daeda90b22cdab5d1758c6cbd4109d5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814071"
---
# <a name="langid-cell-miscellaneous-section"></a>Ячейка LangID (раздел "Прочее")

Указывает язык, на какие ячейки были созданы формулы. 
  
## <a name="remarks"></a>Замечания

Список языков, поддерживаемых приложений Microsoft Office приведены в разделе [DocLangID](doclangid-cell-document-properties-section.md) ячейки (раздел свойства документа). 
  
Для получения ссылки на ячейки LangID по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LangID  <br/> |
   
Для получения ссылки на ячейки LangID по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowMisc** <br/> |
| Индекс ячейки:  <br/> |**visObjLangID** <br/> |
   

