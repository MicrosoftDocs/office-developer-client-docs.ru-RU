---
title: Ячейка TagName (раздел "Действия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60087
localization_priority: Normal
ms.assetid: e593e95d-f975-481d-69cd-619049d4427d
description: Содержит имя тега действия, с которым связана это действие.
ms.openlocfilehash: e1495a34769cbcfdd687491855d1f9c761de2b4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814996"
---
# <a name="tagname-cell-actions-section"></a>Ячейка TagName (раздел "Действия")

Содержит имя тега действия, с которым связана это действие.
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов. 
  
## <a name="remarks"></a>Замечания

Ячейка TagName в разделе действия работает вместе с TagName ячейки в разделе теги действий, чтобы связать тег действия с его действиями. 
  
- Если ячейка TagName в строки действий не задан, отображается действие в контекстном меню выберите не в меню Действие тега.
    
- Если значение ячейки TagName в строке действия совпадает со значением TagName ячейки в строке смарт-тегов, тегов в меню Действие отображается действие.
    
- Если ячейка TagName действия имеет значение, но не соответствует значение TagName в любой строке тег фигуры, это действие не отображается на любой тег действие или контекстного меню.
    
- Если несколько строк смарт-тег с таким же TagName значением, они будут отображать те же действия.
    
Для получения ссылки на ячейки TagName по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |Действия. *имя* . TagNamewhere действия.  *имя* — это имя строки действий  <br/> |
   
Для получения ссылки на ячейки TagName по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionAction** <br/> |
|Индекс строки:  <br/> |**visRowAction** +  *i* где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visActionTagName** <br/> |
   
