---
title: Disabled Cell (Action Tags Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60038
localization_priority: Normal
ms.assetid: bf0a80c9-0fdb-e2cf-3ab0-74cb6338fdce
description: Указывает, отображается ли тег действия в окне документа.
ms.openlocfilehash: 867d36e27cb890509b0687500caf719362a711fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439669"
---
# <a name="disabled-cell-action-tags-section"></a>Disabled Cell (Action Tags Section)

Указывает, отображается ли тег действия в окне документа.
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами. 
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Тег действия отключен.  <br/> |
| FALSE  <br/> | Тег действия включен (значение по умолчанию).  <br/> |
   
## <a name="remarks"></a>Примечания

Если тег действия отключен, он не отображается, пока он не будет повторно включен. 
  
Чтобы получить ссылку на отключенную ячейку по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | SmartTags.  *Name (имя* ). Отключено, где SmartTags. *имя* — название строки тегов действий.  <br/> |
   
Чтобы получить ссылку на отключенную ячейку по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionSmartTag** <br/> |
| Индекс строки:  <br/> |**visRowSmartTag** +  *i*, где *i* = 0, 1, 2…  <br/> |
| Индекс ячейки:  <br/> |**виссмарттагдисаблед** <br/> |
   

