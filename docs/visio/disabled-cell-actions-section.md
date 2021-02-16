---
title: Disabled Cell (Actions Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251337
localization_priority: Normal
ms.assetid: ebf66729-d794-a398-268a-84d761bf06b6
description: Указывает, отключен ли элемент в меню ярлыка или тега действия.
ms.openlocfilehash: ddf55f40056d7df7a2403e500bb4bae335930433
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431353"
---
# <a name="disabled-cell-actions-section"></a>Disabled Cell (Actions Section)

Указывает, отключен ли элемент в меню ярлыка или тега действия.
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Отключение (dim) имени команды.  <br/> |
|FALSE  <br/> |В enable the command name (the default).  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку Disabled по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Действия. *name*  . Отключено, где действия. *имя*  — это имя строки "Действия"  <br/> |
   
Чтобы получить ссылку на ячейку Disabled по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionAction** <br/> |
|Индекс строки:  <br/> |**visRowAction**  +   *i* где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visActionDisabled** <br/> |
   

