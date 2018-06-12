---
title: Ячейка ObjectKind (текстовые поля, раздел)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60058
localization_priority: Normal
ms.assetid: cc4c373c-f073-e3c9-3aaa-a4abf050cd20
description: Указывает тип текстового поля.
ms.openlocfilehash: d4b94b46e83935de14400468957adbdc8f6cb171
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814306"
---
# <a name="objectkind-cell-text-fields-section"></a>Ячейка ObjectKind (текстовые поля, раздел)

Указывает тип текстового поля.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Standard  <br/> |**visTFOKStandard** <br/> |
| 1  <br/> |Горизонтальный в вертикальном  <br/> |**visTFOKHorizontaInVertical** <br/> |
   
## <a name="remarks"></a>Замечания

Текстовые поля может иметь одно из следующих типов:
  
- Стандарт, указывающего на то, что поле был вставлен по категориям поля.
    
- Горизонтальный в вертикальном, указывает, что поле горизонтальный в вертикальном текст.
    
Чтобы получить ссылку на ячейку ObjectKind по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Fields.ObjectKind [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки ObjectKind по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionTextField** <br/> |
| Индекс строки:  <br/> |**visRowField** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visFieldObjectKind** <br/> |
   

