---
title: Transparency Cell (Image Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51095
localization_priority: Normal
ms.assetid: 5b265356-1602-4241-fbe1-4d5a55392a52
description: Определяет уровень прозрачности цвета слоя.
ms.openlocfilehash: defe5307e57c433fcf85a4132939d08cb1ddec77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405837"
---
# <a name="transparency-cell-image-properties-section"></a>Transparency Cell (Image Properties Section)

Определяет уровень прозрачности цвета слоя.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0 - 100  <br/> |Представляет процент прозрачности. По умолчанию — 0% (совершенно непрозрачной).  <br/> |
   
## <a name="remarks"></a>Примечания

Значения округлились до ближайшей половины процента. Значение 100% полностью прозрачно. Несмотря на то, что слой с полностью прозрачным цветом отображается на странице рисования так же, как и слой без цвета, он взаимодействует с другими объектами на странице так же, как если бы его прозрачность была 0%. Это значение можно также установить с помощью управления ползунок в диалоговом окне **Layer Properties** (на вкладке **Home,** в группе редактирования щелкните Слои **и** нажмите кнопку **Layer Properties).** 
  
Чтобы получить ссылку на ячейку Transparency по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Прозрачность  <br/> |
   
Чтобы получить ссылку на ячейку Прозрачности по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowImage** <br/> |
|Индекс ячейки:  <br/> |**visImageTransparency** <br/> |
   

