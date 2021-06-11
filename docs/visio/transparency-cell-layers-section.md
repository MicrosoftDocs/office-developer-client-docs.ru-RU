---
title: Transparency Cell (Layers Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50130
localization_priority: Normal
ms.assetid: 7382e2aa-5e18-19d2-88d8-c4a19a385106
description: Определяет уровень прозрачности цвета слоя.
ms.openlocfilehash: fe0aacf167b2400ca10e22a70c9086429f6059f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436379"
---
# <a name="transparency-cell-layers-section"></a>Transparency Cell (Layers Section)

Определяет уровень прозрачности цвета слоя.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0 - 100  <br/> |Представляет процент прозрачности. По умолчанию — 0% (совершенно непрозрачной).  <br/> |
   
## <a name="remarks"></a>Примечания

Значения округлились до ближайшей половины процента. Значение 100% полностью прозрачно. Несмотря на то, что слой с полностью прозрачным цветом отображается на странице рисования так же, как и слой без цвета, он взаимодействует с другими объектами на странице так же, как если бы его прозрачность была 0%. Это значение можно также установить с помощью управления ползунок в диалоговом окне **Layer Properties** (на вкладке **Home,** в группе редактирования щелкните Слои **и** нажмите кнопку **Layer Properties).** 
  
Чтобы получить ссылку на ячейку Transparency по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Layers.ColorTrans[ *i*  ] где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку Прозрачности по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionLayer** <br/> |
|Индекс строки:  <br/> |**visRowLayer**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
|Индекс ячейки:  <br/> |**visLayerColorTrans** <br/> |
   

