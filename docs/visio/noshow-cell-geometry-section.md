---
title: Ячейка NoShow (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm735
localization_priority: Normal
ms.assetid: 831075ff-2875-b598-00bb-eb8481fee57b
description: Указывает, отображается ли путь на странице документа.
ms.openlocfilehash: ad4d9cf1aa3e541f512bc09ffc38cf03204b3c94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814334"
---
# <a name="noshow-cell-geometry-section"></a>Ячейка NoShow (раздел "Геометрия")

Указывает, отображается ли путь на странице документа.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Числу штрихов и заливки пути, представленный в разделе является скрытым.  <br/> |
| FALSE  <br/> | Показана числу штрихов и заливки пути.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку NoShow по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Геометрия *i* . NoShow где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки NoShow по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**visRowComponent** <br/> |
| Индекс ячейки:  <br/> |**visCompNoShow** <br/> |
   

