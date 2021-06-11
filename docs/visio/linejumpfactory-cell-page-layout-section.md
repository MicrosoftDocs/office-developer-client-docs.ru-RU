---
title: LineJumpFactorY Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm550
localization_priority: Normal
ms.assetid: 5a14be0d-9e3c-23c4-7782-bda5470d1243
description: Определяет размер прыжков строки на вертикальных динамических соединителях на странице относительно значения ячейки LineToLineY. Значение этой ячейки может варьироваться от 0 до 10, но предлагаются дробные значения от 0 до 1.
ms.openlocfilehash: 36712c1558ff2f50309dc31e8f918061180c8fa4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411962"
---
# <a name="linejumpfactory-cell-page-layout-section"></a>LineJumpFactorY Cell (Page Layout Section)

Определяет размер прыжков строки на вертикальных динамических соединителях на странице относительно значения ячейки LineToLineY. Значение этой ячейки может варьироваться от 0 до 10, но предлагаются дробные значения от 0 до 1.
  
## <a name="remarks"></a>Примечания

Вы также можете установить значение этой ячейки на вкладке  Layout и   **Routing** в диалоговом окне Настройка страницы (на вкладке Дизайн щелкните стрелку установки страницы, а затем нажмите макет и маршрутинг).
  
Чтобы получить ссылку на ячейку LineJumpFactorY по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |LineJumpFactorY  <br/> |
   
Чтобы получить ссылку на ячейку LineJumpFactorY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPageLayout** <br/> |
|Индекс ячейки:  <br/> |**visPLOJumpFactorY** <br/> |
   

