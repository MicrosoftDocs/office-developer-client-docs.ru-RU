---
title: BeginGroup Cell (Actions Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60022
localization_priority: Normal
ms.assetid: 1ae7f629-fb9f-1a11-1194-b381d6c9de5b
description: Указывает, вставляется ли разделитель в меню над этим действием.
ms.openlocfilehash: 115dbfe051201dc3ec2b127ff129b077e1067865
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361035"
---
# <a name="begingroup-cell-actions-section"></a>BeginGroup Cell (Actions Section)

Указывает, вставляется ли разделитель в меню над этим действием. 
  
|**Value**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |В меню над этим действием вставляется разделитель.  <br/> |
|FALSE  <br/> |Разделитель не вставляется в меню над этим действием (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку BeginGroup по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Действия. *Name (имя*). BeginGroup, где Actions. *Name* — имя строки действий  <br/> |
   
Чтобы получить ссылку на ячейку BeginGroup по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**Виссектионактион** <br/> |
|Индекс строки:  <br/> |**висровактион** +  *i* , где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**Висактионбегинграуп** <br/> |
   

