---
title: Ячейка Checked (раздел "Действия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm155
localization_priority: Normal
ms.assetid: 50937e29-eaa1-0cd0-53cc-dc17e7793e55
description: Указывает, установлен ли флажок элемента в меню тега ярлык или действие.
ms.openlocfilehash: 7c5bcdbfe5b7d8e796af49c8da6ef0fc233e3d62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813402"
---
# <a name="checked-cell-actions-section"></a>Ячейка Checked (раздел "Действия")

Указывает, установлен ли флажок элемента в меню тега ярлык или действие.
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Галочка.  <br/> |
|FALSE  <br/> |Флажок не отображаются (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на установленное состояние ячейки по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |Действия. *имя* . Где проверяются действия. *имя* — это имя строки действий  <br/> |
   
Для получения ссылки на ячейки установлен по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionAction** <br/> |
|Индекс строки:  <br/> |**visRowAction** +  *i* где *i* = 0, 1, 2,...  <br/> |
|Индекс ячейки:  <br/> |**visActionChecked** <br/> |
   

