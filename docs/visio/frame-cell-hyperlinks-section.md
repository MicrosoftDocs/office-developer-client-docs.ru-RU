---
title: Ячейка Frame (раздел "Гиперссылки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm405
localization_priority: Normal
ms.assetid: f71d8737-92ef-1124-ba4a-b7e17305bd0a
description: Представляет имя frame конечного при открытом как активный документ в приложении контейнера приложения. По умолчанию используется пустая строка.
ms.openlocfilehash: b94e5efd4a3fdf53e01f7518252852214a72c766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813830"
---
# <a name="frame-cell-hyperlinks-section"></a>Ячейка Frame (раздел "Гиперссылки")

Представляет имя frame конечного при открытом как активный документ в приложении контейнера приложения. По умолчанию используется пустая строка.
  
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки Frame с именем, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Гиперссылки.  *имя* . Помещался where гиперссылки.  *имя* — это имя строки  <br/> |
   
Для получения ссылки на ячейки Frame с индекса из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionHyperlink** <br/> |
| Индекс строки:  <br/> |**visRow1stHyperlink** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visHLinkFrame** <br/> |
   

