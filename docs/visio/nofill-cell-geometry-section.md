---
title: NoFill Cell (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm710
localization_priority: Normal
ms.assetid: 0ba7f6da-681b-b749-fe72-afbca23d7e16
description: Указывает, можно ли заполнить путь.
ms.openlocfilehash: 301f30b644e338ff9e597a7a7d8226b9c8a4462f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415021"
---
# <a name="nofill-cell-geometry-section"></a>NoFill Cell (Geometry Section)

Указывает, можно ли заполнить путь.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Путь не заполняется, даже если другие пути в форме заполнены.  <br/> |
| FALSE  <br/> | Заполнение фигуры применяется к пути, даже если он не закрыт.  <br/> |
   
## <a name="remarks"></a>Примечания

Если вы установите шаблон заполнения фигуры ни к одному (0), ни один из его путей не будет заполнен. Эта ячейка используется для выборочного отключения заполнения для пути в форме.
  
Чтобы получить ссылку на ячейку NoFill по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Геометрия  *i*  . NoFill, где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку NoFill по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**visRowComponent** <br/> |
| Индекс ячейки:  <br/> |**visCompNoFill** <br/> |
   

