---
title: PinY ячейки (раздел Преобразование фигуры)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm795
localization_priority: Normal
ms.assetid: 98b86b9d-9cc0-1169-1c44-ef1505bf92fa
description: Представляет y-координата ПИН-код фигуры (центр вращения) относительно начала родительского элемента.
ms.openlocfilehash: 7002415e813ae63dafb64f416079da2e6b170494
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814367"
---
# <a name="piny-cell-shape-transform-section"></a>PinY ячейки (раздел Преобразование фигуры)

Представляет *y* -координата ПИН-код фигуры (центр вращения) относительно начала родительского элемента. 
  
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на PinY ячейки по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | PinY  <br/> |
   
Для получения ссылки на ячейки PinY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowXFormOut** <br/> |
| Индекс ячейки:  <br/> |**visXFormPinY** <br/> |
   

