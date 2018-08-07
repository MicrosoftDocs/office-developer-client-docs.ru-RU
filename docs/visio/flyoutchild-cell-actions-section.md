---
title: Ячейка FlyoutChild (раздел "Действия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80003
localization_priority: Normal
ms.assetid: b2405457-843c-0d46-5f4f-9c413826c3f1
description: Определяет, является ли строку всплывающего меню дочерние последней строки над текстом, который не является дочерним всплывающее меню.
ms.openlocfilehash: 8a41721f91fa9632246e512cfd4ba1a2d871ece5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813784"
---
# <a name="flyoutchild-cell-actions-section"></a>Ячейка FlyoutChild (раздел "Действия")

Определяет, является ли строку всплывающего меню дочерние последней строки над текстом, который не является дочерним всплывающее меню. 
  
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейку с параметром FlyoutChild по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте следующее. 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |Действия. *имя* . FlyoutChildwhere действия.  *имя* — это имя строки действий  <br/> |
   
Для получения ссылки на ячейки с параметром FlyoutChild по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionAction** <br/> |
|Индекс строки:  <br/> |**visRowAction** +  *i* где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visActionFlyoutChild** <br/> |
   

