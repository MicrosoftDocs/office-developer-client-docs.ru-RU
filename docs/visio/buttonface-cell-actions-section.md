---
title: Ячейка ButtonFace (раздел "Действия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60025
localization_priority: Normal
ms.assetid: cf15b879-a47e-a5a5-bfdd-1d7ea423742f
description: Определяет значок, который отображается рядом с элементом меню тега ярлык или действие.
ms.openlocfilehash: 29ff71bc04e94f97f1526b28bd52c2846327eff1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813314"
---
# <a name="buttonface-cell-actions-section"></a>Ячейка ButtonFace (раздел "Действия")

Определяет значок, который отображается рядом с элементом меню тега ярлык или действие.
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов. 
  
## <a name="remarks"></a>Замечания

Строка, содержащихся в ячейке ButtonFace представляет идентификатор изображения кнопки Microsoft Office. Значение нуль (0) или пустая означает, что значок не отображается. 
  
Идентификаторы, которые могут использоваться в ячейке ButtonFace такие же, как идентификаторы, используется совместно со свойством **FaceID** **CommandBarButton** объекта. Для получения дополнительных сведений об этих кодов поиск «работа с изображениями кнопки панели команд» на сайте MSDN. 
  
Чтобы получить ссылку на ячейку ButtonFace по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |**Действия**.  *имя* . **ButtonFace** где **действия**.  *имя* — это имя строки действий  <br/> |
   
Для получения ссылки на ячейки ButtonFace по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionAction** <br/> |
|Индекс строки:  <br/> |**visRowAction** +  *i* где **i** = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visActionButtonFace** <br/> |
   

