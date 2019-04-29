---
title: PrintPageOrientation Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033795
localization_priority: Normal
ms.assetid: f8354d0d-0ce2-fb33-ddf7-611a2c24a8be
description: Определяет, будет ли страница печататься по книжной или альбомной ориентации.
ms.openlocfilehash: f7e73bea5120d878a1b2dbf553a66b349d247fce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434867"
---
# <a name="printpageorientation-cell-print-properties-section"></a>PrintPageOrientation Cell (Print Properties Section)

Определяет, будет ли страница печататься по книжной или альбомной ориентации.
  
|**Значение**|**Orientation**|**Константа автоматизации**|
|:-----|:-----|:-----|
| нуль  <br/> | То же, что принтер  <br/> |**Висппосамеаспринтер** <br/> |
| 1,1  <br/> | Ориентацию  <br/> |**Висппопортраит** <br/> |
|2  <br/> |Вдоль  <br/> |**Виспполандскапе** <br/> |
   
## <a name="remarks"></a>Примечания

При вставке в документ новых страниц этот параметр по умолчанию устанавливается на активной странице.
  
Чтобы получить ссылку на ячейку PrintPageOrientation по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | PrintPageOrientation  <br/> |
   
Чтобы получить ссылку на ячейку PrintPageOrientation по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровпринтпропертиес** <br/> |
| Индекс ячейки:  <br/> |**Виспринтпропертиеспажеориентатион** <br/> |
   

