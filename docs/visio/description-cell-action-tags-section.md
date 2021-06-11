---
title: Description Cell (Action Tags Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60037
localization_priority: Normal
ms.assetid: feb29b91-0f6e-6353-3dd0-7a280843a517
description: Содержит строку, описываемую тегом действий, который отображается в качестве подсказки инструмента при размещении пользователями указателя над тегом.
ms.openlocfilehash: 00c7a4c1547927b8d1a979b8ae074f96f26dc17c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415763"
---
# <a name="description-cell-action-tags-section"></a>Description Cell (Action Tags Section)

Содержит строку, описываемую тегом действий, который отображается в качестве подсказки инструмента при размещении пользователями указателя над тегом.
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку Description по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | SmartTags.  *имя*  . Описание, где SmartTags. *имя* — название строки тегов действий.  <br/> |
   
Чтобы получить ссылку на ячейку Description по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionSmartTag** <br/> |
| Индекс строки:  <br/> |**visRowSmartTag** +  *i*, где *i* = 0, 1, 2…  <br/> |
| Индекс ячейки:  <br/> |**visSmartTagDescription** <br/> |
   

