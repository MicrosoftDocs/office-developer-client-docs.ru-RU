---
title: LangID Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033769
localization_priority: Normal
ms.assetid: c68289b8-ef45-9e1e-12ae-6613587e4990
description: Указывает язык, на котором был введен текст.
ms.openlocfilehash: e1f244d6d8e31201576a9a88ace9701814b0e0a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419284"
---
# <a name="langid-cell-character-section"></a>LangID Cell (Character Section)

Указывает язык, на котором был введен текст. 
  
## <a name="remarks"></a>Примечания

Список языков, поддерживаемых Microsoft Office, см. в разделе [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section). 
  
Чтобы получить ссылку на ячейку LangID по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Char.LangID[  *i*  ] где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку LangID по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionCharacter** <br/> |
| Индекс строки:  <br/> |**visRowCharacter**  +   *i,* *где i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visCharacterLangID** <br/> |
   

