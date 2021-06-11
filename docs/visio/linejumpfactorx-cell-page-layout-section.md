---
title: LineJumpFactorX Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm545
localization_priority: Normal
ms.assetid: 0649672f-f496-ce80-6dc3-3affc9b6f913
description: Определяет размер прыжков строки на горизонтальных динамических соединительнях на странице по отношению к значению ячейки LineToLineX. Значение этой ячейки может варьироваться от 0 до 10, но предлагаются дробные значения от 0 до 1.
ms.openlocfilehash: 8698d99021ca64415417de8e946cbd80b586e759
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424996"
---
# <a name="linejumpfactorx-cell-page-layout-section"></a>LineJumpFactorX Cell (Page Layout Section)

Определяет размер прыжков строки на горизонтальных динамических соединительнях на странице по отношению к значению ячейки LineToLineX. Значение этой ячейки может варьироваться от 0 до 10, но предлагаются дробные значения от 0 до 1.
  
## <a name="remarks"></a>Примечания

Вы также можете установить значение этой ячейки на вкладке  Layout и   **Routing** в диалоговом окне Настройка страницы (на вкладке Дизайн щелкните стрелку установки страницы, а затем нажмите макет и маршрутинг).
  
Чтобы получить ссылку на ячейку LineJumpFactorX по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |LineJumpFactorX  <br/> |
   
Чтобы получить ссылку на ячейку LineJumpFactorX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPageLayout** <br/> |
|Индекс ячейки:  <br/> |**visPLOJumpFactorX** <br/> |
   

