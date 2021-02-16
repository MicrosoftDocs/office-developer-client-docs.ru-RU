---
title: ButtonFace Cell (Actions Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60025
localization_priority: Normal
ms.assetid: cf15b879-a47e-a5a5-bfdd-1d7ea423742f
description: Определяет значок, который отображается рядом с элементом в меню ярлыка или тега действия.
ms.openlocfilehash: 7ee9c4e7e857acb34ce75429aa0aaf679320b0e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407377"
---
# <a name="buttonface-cell-actions-section"></a>ButtonFace Cell (Actions Section)

Определяет значок, который отображается рядом с элементом в меню ярлыка или тега действия.
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами. 
  
## <a name="remarks"></a>Замечания

Строка, содержаная в ячейке ButtonFace, представляет ИД Microsoft Office кнопок. Нулевое (0) или пустое значение означает, что значок не отображается. 
  
ИД, которые можно использовать в ячейке ButtonFace, такие же, как и для свойств **FaceID** объекта **CommandBarButton.** Для получения дополнительных сведений об этих ИД на сайте MSDN найди поиск по запросу "Работа с изображениями кнопок панели команд". 
  
Чтобы получить ссылку на ячейку ButtonFace по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |**Действия**.  *name*  . **ButtonFace,**         где **действия**.  *имя*  — это имя строки действий  <br/> |
   
Чтобы получить ссылку на ячейку ButtonFace по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionAction** <br/> |
|Индекс строки:  <br/> |**visRowAction**  +   *i* где **i** = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visActionButtonFace** <br/> |
   

