---
title: Ячейка Disabled (раздел "Действия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251337
localization_priority: Normal
ms.assetid: ebf66729-d794-a398-268a-84d761bf06b6
description: Указывает, отключена ли пункт меню тега ярлык или действие.
ms.openlocfilehash: 3956b6cf5ccb870255d6943e74b4f02650952d09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813599"
---
# <a name="disabled-cell-actions-section"></a>Ячейка Disabled (раздел "Действия")

Указывает, отключена ли пункт меню тега ярлык или действие.
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Отключите имя команды (dim).  <br/> |
|FALSE  <br/> |Включите имя команды (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку отключено по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |Действия. *имя* . Этот параметр отключен где действия. *имя* — это имя строки действий  <br/> |
   
Для получения ссылки на ячейки отключено по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionAction** <br/> |
|Индекс строки:  <br/> |**visRowAction** +  *i* где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visActionDisabled** <br/> |
   

