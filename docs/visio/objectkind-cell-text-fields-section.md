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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438514"
---
# <a name="objectkind-cell-text-fields-section"></a>ObjectKind Cell (Text Fields Section)

Указывает тип текстового поля.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Стандартный  <br/> |**visTFOKStandard** <br/> |
| 1   <br/> |Горизонтальный по вертикали  <br/> |**visTFOKHorizontaInVertical** <br/> |
   
## <a name="remarks"></a>Примечания

Текстовые поля могут иметь один из следующих типов:
  
- Стандартная, указывающая, что поле было вставлено по категории полей.
    
- По горизонтали по вертикали, указывая, что поле является горизонтальным текстом, установленным в вертикальном тексте.
    
Чтобы получить ссылку на ячейку ObjectKind по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Fields.ObjectKind[  *i*  ] где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку ObjectKind по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionTextField** <br/> |
| Индекс строки:  <br/> |**visRowField**  +   *i,* *где i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visFieldObjectKind** <br/> |
   

