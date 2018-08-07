---
title: Ячейка Description (раздел "Теги действий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60037
localization_priority: Normal
ms.assetid: feb29b91-0f6e-6353-3dd0-7a280843a517
description: Содержит строку, описывающую тег действия, которая отображается в виде подсказки при пользователей поместить их указатель мыши на тег.
ms.openlocfilehash: 3c365d24170f912624a2abdeeadd75140bea9a85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813600"
---
# <a name="description-cell-action-tags-section"></a>Ячейка Description (раздел "Теги действий")

Содержит строку, описывающую тег действия, которая отображается в виде подсказки при пользователей поместить их указатель мыши на тег.
  
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки описание по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Смарт-тегов.  *имя* . Описание где смарт-тегов. *имя* — это имя строки тега действия  <br/> |
   
Для получения ссылки на ячейки описание по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionSmartTag** <br/> |
| Индекс строки:  <br/> |**visRowSmartTag** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visSmartTagDescription** <br/> |
   

