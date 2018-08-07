---
title: Ячейка LangID (раздел "Символ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033769
localization_priority: Normal
ms.assetid: c68289b8-ef45-9e1e-12ae-6613587e4990
description: Указывает язык, на котором был введен текст.
ms.openlocfilehash: e503abb2365635fa25a4dbec54b7fe3da4043fa8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814028"
---
# <a name="langid-cell-character-section"></a>Ячейка LangID (раздел "Символ")

Указывает язык, на котором был введен текст. 
  
## <a name="remarks"></a>Замечания

Список языков, поддерживаемых приложений Microsoft Office приведены в разделе [DocLangID](doclangid-cell-document-properties-section.md) ячейки (раздел свойства документа). 
  
Для получения ссылки на ячейки LangID по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Char.LangID [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки LangID по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionCharacter** <br/> |
| Индекс строки:  <br/> |**visRowCharacter** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visCharacterLangID** <br/> |
   

