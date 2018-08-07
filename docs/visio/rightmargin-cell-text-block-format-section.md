---
title: Ячейка RightMargin (раздел "Формат текстового блока")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251266
localization_priority: Normal
ms.assetid: bc8f5469-e79f-4a68-73cb-d11c938353a4
description: Определяет расстояние между правой границей блока текста и текст, которые он содержит. Значение по умолчанию — 0,1 дюйма.
ms.openlocfilehash: 57fdb320395a9a6562983a0148b37c4a70a9a9b6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814613"
---
# <a name="rightmargin-cell-text-block-format-section"></a>Ячейка RightMargin (раздел "Формат текстового блока")

Определяет расстояние между правой границей блока текста и текст, которые он содержит. Значение по умолчанию — 0,1 дюйма.
  
## <a name="remarks"></a>Замечания

Это значение не зависит от масштаба документа. Если документа изменяется, правое остается неизменным.
  
Для получения ссылки на ячейки RightMargin по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | RightMargin  <br/> |
   
Для получения ссылки на ячейки RightMargin по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowText** <br/> |
| Индекс ячейки:  <br/> |**visTxtBlkRightMargin** <br/> |
   

