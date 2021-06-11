---
title: PlaceFlip Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253251
localization_priority: Normal
ms.assetid: df014b98-cfd5-b6d3-4b8a-b0acb3b94412
description: Определяет, как фигуры переворачиваются и/или вращаются на странице при использовании диалогового окна Настройка макета (на вкладке Дизайн, в группе Макет, щелкните Re-Layout страницу, а затем нажмите кнопку Дополнительные параметры макета).
ms.openlocfilehash: d1c31654782012b3536d35f3a12a923c2cc7a8f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434300"
---
# <a name="placeflip-cell-page-layout-section"></a>PlaceFlip Cell (Page Layout Section)

Определяет, как фигуры переворачиваются и/или вращаются на странице при использовании диалогового окна **Configure Layout** (на вкладке Design, в группе **Макет,** щелкните Страницу повторного макета **и** нажмите кнопку Дополнительные параметры  макета). 
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|&amp;H0  <br/> |Значение, используемое по умолчанию. Не переворачивать.  <br/> |**visLOFlipDefault** <br/> |
|&amp;H1  <br/> |Переверните горизонтально.  <br/> |**visLOFlipX** <br/> |
|&amp;H2  <br/> |Переверните вертикаль.  <br/> |**visLOFlipY** <br/> |
|&amp;H4  <br/> |Flip in 90 degree increments.  <br/> |**visLOFlipRotate** <br/> |
|&amp;H8  <br/> |Не переворачивать.  <br/> |**visLOFlipNone** <br/> |
   
## <a name="remarks"></a>Примечания

Значение в ячейке PlaceFlip помогает сориентировать фигуру на следующую, к ней подключенную. Обычно используется при разработке рисунков с использованием статического клея.
  
Чтобы настроить такое поведение для определенной формы, используйте ячейку ShapePlaceFlip в разделе Макет фигуры.
  
Чтобы получить ссылку на ячейку PlaceFlip по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |PlaceFlip  <br/> |
   
Чтобы получить ссылку на ячейку PlaceFlip по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPageLayout** <br/> |
|Индекс ячейки:  <br/> |**visPLOPlaceFlip** <br/> |
   

