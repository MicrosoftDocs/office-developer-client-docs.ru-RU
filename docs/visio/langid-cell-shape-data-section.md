---
title: LangID Cell (Shape Data Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033771
localization_priority: Normal
ms.assetid: 6bd2781a-d4e7-136f-8996-62ebc5f890ab
description: Указывает язык, на котором ввели значение данных фигуры.
ms.openlocfilehash: c5a0cca5f71bc5520337ad2bdcf354a2b4affe92
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420327"
---
# <a name="langid-cell-shape-data-section"></a>LangID Cell (Shape Data Section)

Указывает язык, на котором ввели значение данных фигуры. 
  
## <a name="remarks"></a>Примечания

Список языков, поддерживаемых Microsoft Office системных приложений, см. в разделе [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section). 
  
Чтобы получить ссылку на ячейку LangID по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Реквизит.  *name*  . LangID, где prop.  *name*  — это имя строки  <br/> |
   
Чтобы получить ссылку на ячейку LangID по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionProp** <br/> |
| Индекс строки:  <br/> |**visRowProp**  +   *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visCustPropsLangID** <br/> |
   

