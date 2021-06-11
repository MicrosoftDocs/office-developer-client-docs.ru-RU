---
title: TextBkgndTrans Cell (Text Block Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253240
localization_priority: Normal
ms.assetid: b2f9d317-cc42-bec5-66f9-f988bcbdcc24
description: Определяет уровень прозрачности фонового цвета текстового блока фигуры.
ms.openlocfilehash: f4c4dc7700c553bd4c9bee337220e357c4c5538a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408693"
---
# <a name="textbkgndtrans-cell-text-block-format-section"></a>TextBkgndTrans Cell (Text Block Format Section)

Определяет уровень прозрачности фонового цвета текстового блока фигуры.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0 - 100  <br/> |Представляет процент прозрачности. По умолчанию — 0% (совершенно непрозрачной).  <br/> |
   
## <a name="remarks"></a>Примечания

Значения округлились до ближайшей половины процента. Значение 100% полностью прозрачно. Несмотря на то, что форма с полностью прозрачным текстовым фоном отображается на странице рисования так же, как и форма без фона текста, она взаимодействует с другими объектами на странице так же, как если бы ее прозрачность была 0%.
  
Вы также можете установить это значение с помощью управления ползунок на вкладке **Шрифт** диалогового окна **Text** (на вкладке **Главная** щелкните **стрелку Шрифта).** 
  
Чтобы получить ссылку на ячейку TextBkgndTrans по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |TextBkgndTrans  <br/> |
   
Чтобы получить ссылку на ячейку TextBkgndTrans по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowText** <br/> |
|Индекс ячейки:  <br/> |**visTxtBlkBkgndTrans** <br/> |
   

