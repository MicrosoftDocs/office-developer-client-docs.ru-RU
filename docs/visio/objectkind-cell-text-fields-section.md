---
title: ObjectKind Cell (Text Fields Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60058
localization_priority: Normal
ms.assetid: cc4c373c-f073-e3c9-3aaa-a4abf050cd20
description: Указывает тип текстового поля.
ms.openlocfilehash: c2f891620f704a3c48861124b886e49d356960ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360993"
---
# <a name="objectkind-cell-text-fields-section"></a>ObjectKind Cell (Text Fields Section)

Указывает тип текстового поля.
  
|**Value**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| нуль  <br/> | Standard  <br/> |**Вистфокстандард** <br/> |
| 1,1  <br/> |Горизонтальный в вертикальном  <br/> |**Вистфокхоризонтаинвертикал** <br/> |
   
## <a name="remarks"></a>Примечания

Текстовые поля могут иметь один из следующих типов:
  
- Standard, указывающая на то, что поле было вставлено по категории полей.
    
- Горизонтальный в вертикальном, указывая, что поле является горизонтальным текстом в вертикальном тексте.
    
Чтобы получить ссылку на ячейку ObjectKind по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Fields. ObjectKind [ *i* ], где *i* = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку ObjectKind по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**Виссектионтекстфиелд** <br/> |
| Индекс строки:  <br/> |**висровфиелд** +  *i* , где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**Висфиелдобжекткинд** <br/> |
   

