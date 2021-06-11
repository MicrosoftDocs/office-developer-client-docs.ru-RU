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
description: Определяет стиль пули.
ms.openlocfilehash: 03b7d046cd42458b614313c19b2100259730539c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422770"
---
# <a name="bullet-cell-paragraph-section"></a>Bullet Cell (Paragraph Section)

Определяет стиль пули.
  
|**Значение**|**Стиль пули**|
|:-----|:-----|
|0  <br/> |Нет  <br/> |
|1  <br/> |![](media/IC_Bullet1_ZA07645847.gif)           <br/> |
|2  <br/> |![](media/IC_Bullet2_ZA07645848.gif)           <br/> |
|3  <br/> |![](media/IC_Bullet3_ZA07645849.gif)           <br/> |
|4   <br/> |![](media/IC_Bullet4_ZA07645851.gif)           <br/> |
|5   <br/> |![](media/IC_Bullet5_ZA07645852.gif)           <br/> |
|6   <br/> |![](media/IC_Bullet6_ZA07645853.gif)           <br/> |
|7   <br/> |![](media/IC_Bullet7_ZA07645854.gif)           <br/> |
   
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionParagraph** <br/> |
|Индекс строки:  <br/> |**visRowParagraph**  +   *i,* *где i* = 0, 1, 2, ...  <br/> |
|Индекс ячейки:  <br/> |**visBulletIndex** <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить значение этой ячейки, щелкнув правой кнопкой мыши фигуру, указав на **формат,** щелкнув **текст,** а затем щелкнув вкладку **Bullets.** 
  
Чтобы получить ссылку на ячейку Bullet по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Para.Bullet[ *i*  ] где  *i*  = <1>, 2, 3, ...  <br/> |
   
Чтобы получить ссылку на ячейку Bullet по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  

