---
title: LineColorTrans Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50120
localization_priority: Normal
ms.assetid: b68054b5-7efd-1156-9dc1-5ec94e18d227
description: Определяет уровень прозрачности цвета строки фигуры.
ms.openlocfilehash: 555ea15de0279a37bcf67de7374d922b8692ce02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414440"
---
# <a name="linecolortrans-cell-line-format-section"></a>LineColorTrans Cell (Line Format Section)

Определяет уровень прозрачности цвета строки фигуры.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0 - 100  <br/> |Представляет процент прозрачности. По умолчанию — 0% (совершенно непрозрачной).  <br/> |
   
## <a name="remarks"></a>Примечания

Значения округлились до ближайшей половины процента. Значение 100% полностью прозрачно. Хотя фигура с полностью прозрачным цветом строки выглядит так же, как фигура без линий на странице рисования, она будет взаимодействовать с другими объектами на странице так же, как если бы ее прозрачность составляет 0%. 
  
Это значение можно также задать с помощью управления ползунок в диалоговом окне **Line** (на вкладке **Главная,** в группе **Shape** щелкните Строка, указать на **вес,** а затем нажмите кнопку **Дополнительные строки).**
  
Чтобы получить ссылку на ячейку LineColorTrans по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |LineColorTrans  <br/> |
   
Чтобы получить ссылку на ячейку LineColorTrans по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowLine** <br/> |
|Индекс ячейки:  <br/> |**visLineColorTrans** <br/> |
   

