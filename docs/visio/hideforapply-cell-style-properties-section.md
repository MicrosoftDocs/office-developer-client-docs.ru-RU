---
title: HideForApply Cell (Style Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251698
localization_priority: Normal
ms.assetid: 62d87db9-b8ca-60b6-bf27-5168c718ec96
description: Определяет, где отображается стиль в пользовательском интерфейсе Microsoft Visio.
ms.openlocfilehash: 7b3830488770a66d7be35923e1807dbcdcd1f1c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329955"
---
# <a name="hideforapply-cell-style-properties-section"></a>HideForApply Cell (Style Properties Section)

Определяет, где отображается стиль в пользовательском интерфейсе Microsoft Visio.
  
|**Value**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Отображение стиля только в проводнике по **документам**.  <br/> |
| FALSE  <br/> | Отображение стиля в проводнике по **документам**.  <br/> |
   
## <a name="remarks"></a>Комментарии

Когда вы создаете новый стиль для скрытого стиля, новый стиль не наследует этот атрибут.
  
Чтобы получить ссылку на ячейку HideForApply по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | HideForApply  <br/> |
   
Чтобы получить ссылку на ячейку HideForApply по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровстиле** <br/> |
| Индекс ячейки:  <br/> |**Висстилехидден** <br/> |
   

