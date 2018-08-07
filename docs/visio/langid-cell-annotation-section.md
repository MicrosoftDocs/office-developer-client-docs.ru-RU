---
title: Ячейка LangID (раздел "Примечание")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60048
localization_priority: Normal
ms.assetid: b6f5ea5e-b350-0817-d631-f059b9b95c23
description: Указывает язык, в котором был введен комментарий.
ms.openlocfilehash: 0de5ed8136a3fb1bbdca9fea0ebb5894e62cf907
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814032"
---
# <a name="langid-cell-annotation-section"></a>Ячейка LangID (раздел "Примечание")

Указывает язык, в котором был введен комментарий.
  
> [!NOTE]
> В этой ячейке используется для контроля комментариев только при открытии VSD-файл в Microsoft Visio 2013 или при сохранении файла vsdx (en) в формате .vsd. Он не используется для отслеживания комментариев в документах vsdx (en) в Visio 2013. 
  
## <a name="remarks"></a>Замечания

Это значение — код языка (LCID) языка, который является активным на панели языка при вводе комментария. Список языков, поддерживаемых приложений Microsoft Office приведены в разделе [DocLangID](doclangid-cell-document-properties-section.md) ячейки (раздел свойства документа). 
  
Для получения ссылки на ячейки LangID по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Annotation.LangID [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки LangID по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionAnnotation** <br/> |
| Индекс строки:  <br/> |**visRowAnnotation** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visAnnotationLangID** <br/> |
   

