---
title: Frame Cell (Hyperlinks Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm405
localization_priority: Normal
ms.assetid: f71d8737-92ef-1124-ba4a-b7e17305bd0a
description: Представляет имя целевого кадра, когда приложение открыто как активный документ в контейнерном приложении. Значение по умолчанию — пустая строка.
ms.openlocfilehash: 8f41e5bf854e31e1f17eabb2aecbded55175ebaf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432858"
---
# <a name="frame-cell-hyperlinks-section"></a>Frame Cell (Hyperlinks Section)

Представляет имя целевого кадра, когда приложение открыто как активный документ в контейнерном приложении. Значение по умолчанию — пустая строка.
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку Frame по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Гиперссылки.  *Name (имя* ). Frame с гиперссылкой.  *Name* — имя строки  <br/> |
   
Чтобы получить ссылку на ячейку Frame по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**Виссектионхиперлинк** <br/> |
| Индекс строки:  <br/> |**visRow1stHyperlink** +  *i* , где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**Вишлинкфраме** <br/> |
   

