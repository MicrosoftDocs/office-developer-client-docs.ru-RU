---
title: PlaceStyle Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dcd5a35-bd3d-447f-e4aa-986091d129de
description: Определяет, как фигуры размещаются на странице при выкладке фигур с помощью диалогового окна Настройка макета (на вкладке Дизайн, в группе Макет нажмите кнопку Re-Layout Page, а затем нажмите кнопку Дополнительные параметры макета).
ms.openlocfilehash: b3159b765922d6656d12dd42a377322e4a91fc04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420803"
---
# <a name="placestyle-cell-page-layout-section"></a>PlaceStyle Cell (Page Layout Section)

Определяет, как фигуры размещаются на странице при выкладке фигур с помощью  диалогового окна **Настройка** макета (на вкладке Дизайн, в группе **Макет,** нажмите страницу повторного макета, а затем нажмите кнопку Дополнительные параметры макета). 
  
## <a name="remarks"></a>Примечания

Вы также можете установить значение этой ячейки в диалоговом окне **Настройка** макета. 
  
Чтобы получить ссылку на ячейку PlaceStyle по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |PlaceStyle  <br/> |
   
Чтобы получить ссылку на ячейку PlaceStyle по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPageLayout** <br/> |
|Индекс ячейки:  <br/> |**visPLOPlaceStyle** <br/> |
   

