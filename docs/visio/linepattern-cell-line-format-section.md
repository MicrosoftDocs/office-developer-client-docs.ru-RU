---
title: LinePattern Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm560
localization_priority: Normal
ms.assetid: a416762b-7294-c99f-d9f1-332c3ed35dff
description: Определяет шаблон линии фигуры. Значение, введенное в ячейке LinePattern, — это число, которое является индексом в коллекции шаблонов строк.
ms.openlocfilehash: eec5bed18777f7822f9544d59dce7722f2f732bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316445"
---
# <a name="linepattern-cell-line-format-section"></a>LinePattern Cell (Line Format Section)

Определяет шаблон линии фигуры. Значение, введенное в ячейке LinePattern, — это число, которое является индексом в коллекции шаблонов строк.
  
|**Value**|**Описание**|
|:-----|:-----|
|нуль  <br/> |Без шаблона линии  <br/> |
|1,1  <br/> |Сплошная  <br/> |
|2-23  <br/> |Шаблоны строк для ассортимента  <br/> |
   
## <a name="remarks"></a>Замечания

Вы можете просмотреть коллекцию шаблонов линий в диалоговом окне **линия** (на вкладке **Главная** , в группе **фигура** , щелкните **линия**, выберите штрихи и нажмите **** кнопку **другие линии**).
  
Чтобы указать настраиваемый шаблон линии, используйте функцию USE в этой ячейке.
  
Чтобы получить ссылку на ячейку LinePattern по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |LinePattern  <br/> |
   
Чтобы получить ссылку на ячейку LinePattern по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**Висровлине** <br/> |
|Индекс ячейки:  <br/> |**Вислинепаттерн** <br/> |
   

