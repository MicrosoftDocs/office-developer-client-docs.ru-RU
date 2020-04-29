---
title: FlyoutChild Cell (Actions Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80003
localization_priority: Normal
ms.assetid: b2405457-843c-0d46-5f4f-9c413826c3f1
description: Определяет, является ли строка дочерним всплывающим меню последней строки над ним, которое не является потомком всплывающего списка.
ms.openlocfilehash: 85524ea33258449f5c9ee0991ac9a64f8f0eebae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420866"
---
# <a name="flyoutchild-cell-actions-section"></a>FlyoutChild Cell (Actions Section)

Определяет, является ли строка дочерним всплывающим меню последней строки над ним, которое не является потомком всплывающего списка. 
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку FlyoutChild по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Действия. *Name (имя* ). Действия Флйоутчилдвхере.  *Name* — имя строки действий  <br/> |
   
Чтобы получить ссылку на ячейку FlyoutChild по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**виссектионактион** <br/> |
|Индекс строки:  <br/> |**висровактион** +  *i* , где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**висактионфлйоутчилд** <br/> |
   

