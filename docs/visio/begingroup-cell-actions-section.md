---
title: Ячейка BeginGroup (раздел "Действия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60022
localization_priority: Normal
ms.assetid: 1ae7f629-fb9f-1a11-1194-b381d6c9de5b
description: Указывает, будет ли разделитель вставлен в меню над это действие.
ms.openlocfilehash: 749f611209d362811f5e4fb051780a4a642295c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813179"
---
# <a name="begingroup-cell-actions-section"></a>Ячейка BeginGroup (раздел "Действия")

Указывает, будет ли разделитель вставлен в меню над это действие. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Разделитель в меню над это действие.  <br/> |
|FALSE  <br/> |Разделитель не вставляется в меню над это действие (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку BeginGroup по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |Действия. *имя*. BeginGroup где действия. *имя* — это имя строки действий  <br/> |
   
Для получения ссылки на ячейки BeginGroup по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionAction** <br/> |
|Индекс строки:  <br/> |**visRowAction** +  *i* где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visActionBeginGroup** <br/> |
   

