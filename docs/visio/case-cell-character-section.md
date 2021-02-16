---
title: Case Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251250
localization_priority: Normal
ms.assetid: cf063c05-5789-e037-700b-1e70df00e254
description: Определяет случай текста фигуры. Все заголовочные (верхние) буквы (1) и начальные буквы (2) не изменяют внешний вид текста, введенного во всех заголовных буквах. Чтобы эти параметры вступили в силу, текст должен быть введен в нижнем регистре.
ms.openlocfilehash: 50ceaa1188caded40d36b8837c346fbbba2e14d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434349"
---
# <a name="case-cell-character-section"></a>Case Cell (Character Section)

Определяет случай текста фигуры. Все заголовочные (верхние) буквы (1) и начальные буквы (2) не изменяют внешний вид текста, введенного во всех заголовных буквах. Чтобы эти параметры вступили в силу, текст должен быть введен в нижнем регистре.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Обычный случай  <br/> |**visCaseNormal** <br/> |
| 1   <br/> | Все буквы в верхнем регистре  <br/> |**visCaseAllCaps** <br/> |
| 2   <br/> | Только начальные буквы  <br/> |**visCaseInitialCaps** <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку Case по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Char.Case[  *i*  ] где  *i*  = <1>, 2, 3, ...  <br/> |
   
Чтобы получить ссылку на ячейку Case по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionCharacter** <br/> |
| Индекс строки:  <br/> |**visRowCharacter**  +   *i* где *i* = 0, 1, 2, ...  <br/> |
| Индекс ячейки:  <br/> |**visCharacterCase** <br/> |
   

