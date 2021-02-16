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
description: Указывает, вставлен ли в меню над этим действием сепаратор.
ms.openlocfilehash: 115dbfe051201dc3ec2b127ff129b077e1067865
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407839"
---
# <a name="begingroup-cell-actions-section"></a>BeginGroup Cell (Actions Section)

Указывает, вставлен ли в меню над этим действием сепаратор. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |В меню над этим действием вставляется сепаратор.  <br/> |
|FALSE  <br/> |В меню над этим действием не вставляется сепаратор (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку BeginGroup по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Действия. *name*. BeginGroup, где действия. *имя* — это имя строки "Действия"  <br/> |
   
Чтобы получить ссылку на ячейку BeginGroup по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionAction** <br/> |
|Индекс строки:  <br/> |**visRowAction**  +   *i,* *где i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visActionBeginGroup** <br/> |
   

