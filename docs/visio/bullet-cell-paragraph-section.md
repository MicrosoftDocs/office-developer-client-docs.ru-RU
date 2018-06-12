---
title: Маркер ячейки (раздел абзаца)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm130
localization_priority: Normal
ms.assetid: 124a5ee1-6dd1-d17d-6f0e-dbaa5d95d9cd
description: Определяет стиль маркеров.
ms.openlocfilehash: d3ecdd8e0f3780490f92766351b5ac94e875ae28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813318"
---
# <a name="bullet-cell-paragraph-section"></a>Маркер ячейки (раздел абзаца)

Определяет стиль маркеров.
  
|**Значение**|**Стиль маркированного списка**|
|:-----|:-----|
|0  <br/> |Нет  <br/> |
|1  <br/> |![](media/IC_Bullet1_ZA07645847.gif)           <br/> |
|2  <br/> |![](media/IC_Bullet2_ZA07645848.gif)           <br/> |
|3  <br/> |![](media/IC_Bullet3_ZA07645849.gif)           <br/> |
|4  <br/> |![](media/IC_Bullet4_ZA07645851.gif)           <br/> |
|5  <br/> |![](media/IC_Bullet5_ZA07645852.gif)           <br/> |
|6  <br/> |![](media/IC_Bullet6_ZA07645853.gif)           <br/> |
|7  <br/> |![](media/IC_Bullet7_ZA07645854.gif)           <br/> |
   
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionParagraph** <br/> |
|Индекс строки:  <br/> |**visRowParagraph** +  *i* где *i* = 0, 1, 2,...  <br/> |
|Индекс ячейки:  <br/> |**visBulletIndex** <br/> |
   
## <a name="remarks"></a>Замечания

Вы может также необходимо задать значение ячейки, щелкнув правой кнопкой мыши фигуру, с указанием **формате**, нажав кнопку **текст**и затем выбрав вкладку **маркеры** . 
  
Для получения ссылки на ячейку маркера по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |Para.Bullet [ *i* ] где *i* = < 1 > 2, 3,...  <br/> |
   
Для получения ссылки на ячейки маркера по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  

