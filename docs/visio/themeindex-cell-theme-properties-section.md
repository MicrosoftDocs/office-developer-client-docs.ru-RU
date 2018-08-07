---
title: Ячейка ThemeIndex (раздел "Свойства темы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: Сохранение перечисление встроенных темы Microsoft Visio, примененная к документу, как целое число. При выборе новой темы для документа, ячейка ThemeIndex для документа и всех страниц и фигур которые он содержит обновляется индекс встроенных темы.
ms.openlocfilehash: 8a9202631bc4d9131d52dea1f852983e1d7528e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815013"
---
# <a name="themeindex-cell-theme-properties-section"></a>Ячейка ThemeIndex (раздел "Свойства темы")

Сохранение перечисление встроенных темы Microsoft Visio, примененная к документу, как целое число. При новой темы выбран для документа ячейки **ThemeIndex** для документа и всех страниц и фигуры, которые он содержит обновляется с индексом встроенных темы. 
  
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки **ThemeIndex** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | ThemeIndex  <br/> |
   
Для получения ссылки на ячейки **ThemeIndex** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowThemeProperties** <br/> |
| Индекс ячейки:  <br/> |**visThemeIndex** <br/> |
   

