---
title: Ячейка UICode (раздел "Текстовые поля")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1075
localization_priority: Normal
ms.assetid: 1d9717c1-4310-0d62-874f-4df77cd81627
description: Определяет код, вставленный поля в версии Visio, предшествующие Visio 2000.
ms.openlocfilehash: ce05f779bfebd5720555f1a2d92b1f9f92cfbdfd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815094"
---
# <a name="uicode-cell-text-fields-section"></a>Ячейка UICode (раздел "Текстовые поля")

Определяет код, вставленный поля в версии Visio, предшествующие Visio 2000.
  
## <a name="remarks"></a>Замечания

В этой ячейке не отображается в окне таблицы свойств фигуры. Используйте эту ячейку, если вам потребуется работать с возможностью обратной проблем, таких как сохранение версии 2000 документ Visio в формат файлов Visio версии 5.0.
  
Чтобы получить ссылку на ячейку UICode по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Fields.UICod [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки UICode по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionTextField** <br/> |
| Индекс строки:  <br/> |**visRowField** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visFieldUICode** <br/> |
   

