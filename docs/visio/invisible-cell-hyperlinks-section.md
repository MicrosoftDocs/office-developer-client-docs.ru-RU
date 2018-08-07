---
title: Ячейка Invisible (раздел "Гиперссылки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033755
localization_priority: Normal
ms.assetid: e67dcd83-4a88-a0f8-5c6a-dae51424edbd
description: Указывает, отображается ли гиперссылка в контекстном меню для фигуры или страницы.
ms.openlocfilehash: e269c5e907afa0d49f1fc6115b7a031835467c2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813979"
---
# <a name="invisible-cell-hyperlinks-section"></a>Ячейка Invisible (раздел "Гиперссылки")

Указывает, отображается ли гиперссылка в контекстном меню для фигуры или страницы. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Гиперссылка не отображается в виде элемента меню в контекстном меню.  <br/> |
|FALSE  <br/> |Гиперссылки отображаются в виде элемента меню в контекстном меню (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки невидимой по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |Гиперссылки. *имя* . Невидимое, где гиперссылки *.name* — это имя строки  <br/> |
   
Для получения ссылки на ячейки невидимой по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionHyperlink** <br/> |
|Индекс строки:  <br/> |**visRow1stHyperlink** +  *i* где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visHLinkInvisible** <br/> |
   

