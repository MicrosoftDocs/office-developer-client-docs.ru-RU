---
title: Bullet Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm130
localization_priority: Normal
ms.assetid: 124a5ee1-6dd1-d17d-6f0e-dbaa5d95d9cd
description: Определяет стиль маркеров.
ms.openlocfilehash: 03b7d046cd42458b614313c19b2100259730539c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338201"
---
# <a name="bullet-cell-paragraph-section"></a>Bullet Cell (Paragraph Section)

Определяет стиль маркеров.
  
|**Значение**|**Стиль маркеров**|
|:-----|:-----|
|нуль  <br/> |Нет  <br/> |
|1,1  <br/> |![](media/IC_Bullet1_ZA07645847.gif)           <br/> |
|2  <br/> |![](media/IC_Bullet2_ZA07645848.gif)           <br/> |
|4  <br/> |![](media/IC_Bullet3_ZA07645849.gif)           <br/> |
|SP4  <br/> |![](media/IC_Bullet4_ZA07645851.gif)           <br/> |
|17:00  <br/> |![](media/IC_Bullet5_ZA07645852.gif)           <br/> |
|ICMPv6  <br/> |![](media/IC_Bullet6_ZA07645853.gif)           <br/> |
|см  <br/> |![](media/IC_Bullet7_ZA07645854.gif)           <br/> |
   
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**Виссектионпараграф** <br/> |
|Индекс строки:  <br/> |**висровпараграф** +  *i* , где *i* = 0, 1, 2,...  <br/> |
|Индекс ячейки:  <br/> |**Висбуллетиндекс** <br/> |
   
## <a name="remarks"></a>Комментарии

Можно также задать значение этой ячейки, щелкнув фигуру правой кнопкой мыши, выбрав пункт **Формат**, пункт **текст**, а затем выбрав вкладку **маркеры** . 
  
Чтобы получить ссылку на ячейку маркера по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Para. Bullet [ *i* ], где *i* = <1>, 2, 3,...  <br/> |
   
Чтобы получить ссылку на ячейку маркера по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  

