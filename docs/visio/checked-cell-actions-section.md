---
title: Checked Cell (Actions Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm155
localization_priority: Normal
ms.assetid: 50937e29-eaa1-0cd0-53cc-dc17e7793e55
description: Указывает, отмечен ли элемент в контекстном меню или меню тегов действий.
ms.openlocfilehash: 870823f28d802e7cafa81efbe5617f27b6714885
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341848"
---
# <a name="checked-cell-actions-section"></a>Checked Cell (Actions Section)

Указывает, отмечен ли элемент в контекстном меню или меню тегов действий.
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами. 
  
|**Value**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Отображается галочка.  <br/> |
|FALSE  <br/> |Галочка не отображается (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Комментарии

Чтобы получить ссылку на возвращенную ячейку по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Действия. *Name (имя* ). Отмеченные действия. *Name* — имя строки действий  <br/> |
   
Чтобы получить ссылку на отмеченную ячейку по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**Виссектионактион** <br/> |
|Индекс строки:  <br/> |**висровактион** +  *i* , где *i* = 0, 1, 2,...  <br/> |
|Индекс ячейки:  <br/> |**Висактиончеккед** <br/> |
   

