---
title: HideText Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251323
localization_priority: Normal
ms.assetid: 3d23647a-e567-da71-50df-336a0f2f4071
description: Скрывает текст для фигуры. Вы можете просматривать текст, изменять свойства и применять стили к тексту в блоке текста, несмотря на то, что изменения не будут отображаться до сброса HideText в значение FALSE (0).
ms.openlocfilehash: 3e1be814984ed15247c451f5cd86d0f7a6dba71a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329962"
---
# <a name="hidetext-cell-miscellaneous-section"></a>HideText Cell (Miscellaneous Section)

Скрывает текст для фигуры. Вы можете просматривать текст, изменять свойства и применять стили к тексту в блоке текста, несмотря на то, что изменения не будут отображаться до сброса HideText в значение FALSE (0).
  
|**Value**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Текст скрыт и не печатается.  <br/> |
| FALSE  <br/> | Текст не скрыт.  <br/> |
   
## <a name="remarks"></a>Комментарии

Чтобы получить ссылку на ячейку HideText по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | HideText  <br/> |
   
Чтобы получить ссылку на ячейку HideText по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровмиск** <br/> |
| Индекс ячейки:  <br/> |**Вишидетекст** <br/> |
   

