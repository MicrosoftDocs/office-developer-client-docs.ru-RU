---
title: Invisible Cell (Actions Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60046
localization_priority: Normal
ms.assetid: 070b4468-c907-b201-1633-1d3e10ecc2b2
description: Указывает, отображается ли действие в теге действия или в контекстном меню.
ms.openlocfilehash: 69bc96e76f27a64d6e1443f045c27566f598c1db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297244"
---
# <a name="invisible-cell-actions-section"></a>Invisible Cell (Actions Section)

Указывает, отображается ли действие в теге действия или в контекстном меню. 
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами. 
  
|**Value**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Действие не отображается в меню.  <br/> |
|FALSE  <br/> |Действие отображается в меню (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на неВидимую ячейку по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Действия. *Name (имя* ). Действия Инвисиблевхере.  *Name* — имя строки действий  <br/> |
   
Чтобы получить ссылку на неВидимую ячейку по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**Виссектионактион** <br/> |
|Индекс строки:  <br/> |**висровактион** +  *i* , где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**Висактионинвисибле** <br/> |
   

