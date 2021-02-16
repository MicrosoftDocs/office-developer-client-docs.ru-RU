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
description: Определяет, является ли строка "child flyout menu" последней строки над ней, которая не является его дитя.
ms.openlocfilehash: 85524ea33258449f5c9ee0991ac9a64f8f0eebae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420866"
---
# <a name="flyoutchild-cell-actions-section"></a>FlyoutChild Cell (Actions Section)

Определяет, является ли строка "child flyout menu" последней строки над ней, которая не является его дитя. 
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку FlyoutChild по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте следующую ссылку. 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Действия. *name*  . Действия FlyoutChildwhere.  *имя*  — это имя строки "Действия"  <br/> |
   
Чтобы получить ссылку на ячейку FlyoutChild по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionAction** <br/> |
|Индекс строки:  <br/> |**visRowAction**  +   *i,* *где i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visActionFlyoutChild** <br/> |
   

