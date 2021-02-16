---
title: ReadOnly Cell (Actions Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60071
localization_priority: Normal
ms.assetid: 158b4188-570c-3817-bf34-8dc0c64befa5
description: Управляет тем, является ли действие над тегом действия или ярлыком меню только для чтения.
ms.openlocfilehash: f45f22001a4d7275bb9367414c8b04ea3c0d9c6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434237"
---
# <a name="readonly-cell-actions-section"></a>ReadOnly Cell (Actions Section)

Управляет тем, является ли действие над тегом действия или ярлыком меню только для чтения. 
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Действие отображается в меню, но только для чтения.  <br/> |
|FALSE  <br/> |Действие отображается в меню и может быть выбрано (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Примечания

Если действие находится только для чтения, оно отображается в теге действия или в ярлыке меню, но его невозможно выбрать. Оно не затемнено, а отображается на цветном фоне, как метка. Чтобы элемент меню стал неамерованным, используйте ячейку Disabled. 
  
Чтобы получить ссылку на ячейку ReadOnly по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Действия. *name*  . ReadOnlywhere Actions.  *имя*  — это имя строки "Действия".  <br/> |
   
Чтобы получить ссылку на ячейку ReadOnly по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionAction** <br/> |
|Индекс строки:  <br/> |**visRowAction**  +   *i* где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visActionReadOnly** <br/> |
   

