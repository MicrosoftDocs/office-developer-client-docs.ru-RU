---
title: Ячейка LangID (раздел "Данные фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033771
localization_priority: Normal
ms.assetid: 6bd2781a-d4e7-136f-8996-62ebc5f890ab
description: Указывает язык, в котором было введено значение данных фигуры.
ms.openlocfilehash: 696c42483390509474eb82bd8cc0046beee345e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814051"
---
# <a name="langid-cell-shape-data-section"></a>Ячейка LangID (раздел "Данные фигуры")

Указывает язык, в котором было введено значение данных фигуры. 
  
## <a name="remarks"></a>Замечания

Список языков, поддерживаемых приложениях системы Microsoft Office в разделе [DocLangID](doclangid-cell-document-properties-section.md) ячейки (раздел свойства документа). 
  
Для получения ссылки на ячейки LangID по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Свойства.  *имя* . LangID где свойств.  *имя* — это имя строки  <br/> |
   
Для получения ссылки на ячейки LangID по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionProp** <br/> |
| Индекс строки:  <br/> |**visRowProp** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visCustPropsLangID** <br/> |
   

