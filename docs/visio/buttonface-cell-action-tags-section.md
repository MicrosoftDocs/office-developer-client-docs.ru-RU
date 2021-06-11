---
title: ButtonFace Cell (Action Tags Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60026
localization_priority: Normal
ms.assetid: 26f370e1-5193-f47d-7b60-3597975be650
description: Содержит ID изображения лица кнопки, которое отображается на кнопке тег действия.
ms.openlocfilehash: e74b3281d894cebd8491112181198d427f0d337f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337542"
---
# <a name="buttonface-cell-action-tags-section"></a>ButtonFace Cell (Action Tags Section)

Содержит ID изображения лица кнопки, которое отображается на кнопке тег действия. 
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами. 
  
## <a name="remarks"></a>Замечания

Строка, содержалась в ячейке ButtonFace, представляет собой ID изображения Microsoft Office кнопки. Значение 0 (ноль) или пустые по умолчанию на стандартную кнопку "i" ![Стандартная кнопка "i"](media/InfoPS_ZA10180114.gif).
  
ИД, которые можно использовать в ячейке ButtonFace, такие же, как ИД, используемые с свойством **FaceID** объекта **CommandBarButton.** Дополнительные сведения об этих ID-кодах можно найти в MSDN для поиска "работы с изображениями кнопки панели команд". 
  
Чтобы получить ссылку на ячейку ButtonFace по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | SmartTags.  *имя*  . ButtonFace, где SmartTags. *имя* — название строки тегов действий.  <br/> |
   
Чтобы получить ссылку на ячейку ButtonFace по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionSmartTag** <br/> |
| Индекс строки:  <br/> |**visRowSmartTag** +  *i*, где *i* = 0, 1, 2…  <br/> |
| Индекс ячейки:  <br/> |**visSmartTagButtonFace** <br/> |
   

