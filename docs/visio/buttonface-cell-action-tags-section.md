---
title: Ячейка ButtonFace (раздел "Теги действий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60026
localization_priority: Normal
ms.assetid: 26f370e1-5193-f47d-7b60-3597975be650
description: Содержит идентификатор изображения кнопки, которое отображается на кнопке тега действия.
ms.openlocfilehash: e74b3281d894cebd8491112181198d427f0d337f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385482"
---
# <a name="buttonface-cell-action-tags-section"></a>Ячейка ButtonFace (раздел "Теги действий")

Содержит идентификатор изображения кнопки, которое отображается на кнопке тега действия. 
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами. 
  
## <a name="remarks"></a>Замечания

Строка, содержащихся в ячейке ButtonFace представляет идентификатор изображения кнопки Microsoft Office. Значение нуль (0) или пустые значения по умолчанию для кнопки стандартного действия тег «я» info ![Кнопки info тега «я» Standard действия](media/InfoPS_ZA10180114.gif).
  
Идентификаторы, которые могут использоваться в ячейке ButtonFace такие же, как идентификаторы, используется совместно со свойством **FaceID** **CommandBarButton** объекта. Для получения дополнительных сведений об этих кодов поиск «работа с изображениями кнопки панели команд» на сайте MSDN. 
  
Для получения ссылки на ячейки ButtonFace по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | SmartTags.  *имя* . ButtonFace где смарт-тегов. *имя* — название строки тегов действий.  <br/> |
   
Для получения ссылки на ячейки ButtonFace по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionSmartTag** <br/> |
| Индекс строки:  <br/> |**visRowSmartTag** +  *i*, где *i* = 0, 1, 2…  <br/> |
| Индекс ячейки:  <br/> |**visSmartTagButtonFace** <br/> |
   

