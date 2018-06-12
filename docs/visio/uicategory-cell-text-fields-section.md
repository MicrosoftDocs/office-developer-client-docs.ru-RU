---
title: Ячейка UICategory (текстовые поля, раздел)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1070
localization_priority: Normal
ms.assetid: 365f7005-ba34-2311-4c5c-16344962fc3f
description: Определяет категории вставленный поля в версии Visio, предшествующие Visio 2000.
ms.openlocfilehash: fc060ac1533732749d10e1855dc3841602051520
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815099"
---
# <a name="uicategory-cell-text-fields-section"></a>Ячейка UICategory (текстовые поля, раздел)

Определяет категории вставленный поля в версии Visio, предшествующие Visio 2000.
  
## <a name="remarks"></a>Замечания

В этой ячейке не отображается в окне таблицы свойств фигуры. Используйте эту ячейку, если вам потребуется работать с обратной возможность проблемы, такие как сохранение версии 2000 документ Visio в формат файлов Visio версии 5.0.
  
Чтобы получить ссылку на ячейку UICategory по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Fields.UICat [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки UICategory по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionTextField** <br/> |
| Индекс строки:  <br/> |**visRowField** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visFieldUICategory** <br/> |
   

