---
title: Ячейка UIFormat (раздел "Текстовые поля")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1080
localization_priority: Normal
ms.assetid: 0dddef20-c58e-2306-ab8e-6cac8e159f61
description: Определяет формат вставленного поля в версии Visio, предшествующие Visio 2000.
ms.openlocfilehash: e9506404e8ccd6ae4452c10ecdcce2d4dfd7ac2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815117"
---
# <a name="uiformat-cell-text-fields-section"></a>Ячейка UIFormat (раздел "Текстовые поля")

Определяет формат вставленного поля в версии Visio, предшествующие Visio 2000.
  
## <a name="remarks"></a>Замечания

В этой ячейке не отображается в окне таблицы свойств фигуры. Используйте эту ячейку, если вам потребуется работать с возможностью обратной проблем, таких как сохранение версии 2000 документ Visio в формат файлов Visio версии 5.0.
  
Чтобы получить ссылку на ячейку UIFormat по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Fields.UIFmt [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки UIFormat по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionTextField** <br/> |
| Индекс строки:  <br/> |**visRowField** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visFieldUIFormat** <br/> |
   

