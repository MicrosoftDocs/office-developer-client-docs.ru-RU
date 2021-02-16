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
description: Указывает, проверяется ли элемент в меню ярлыка или тега действия.
ms.openlocfilehash: 870823f28d802e7cafa81efbe5617f27b6714885
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438332"
---
# <a name="checked-cell-actions-section"></a>Checked Cell (Actions Section)

Указывает, проверяется ли элемент в меню ярлыка или тега действия.
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Отображается контрольная метка.  <br/> |
|FALSE  <br/> |Check mark is not displayed (the default).  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку Checked по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Действия. *name*  . Проверяется, где действия. *имя*  — это имя строки "Действия".  <br/> |
   
Чтобы получить ссылку на ячейку Checked по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionAction** <br/> |
|Индекс строки:  <br/> |**visRowAction**  +   *i* где *i* = 0, 1, 2, ...  <br/> |
|Индекс ячейки:  <br/> |**visActionChecked** <br/> |
   

