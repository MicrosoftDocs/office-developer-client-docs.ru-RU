---
title: Ячейка BulletString (раздел "Абзац")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm135
localization_priority: Normal
ms.assetid: 38285824-30ad-0cf2-07cb-0103ab3a415a
description: Позволяет создавать пользовательские стили маркеров.
ms.openlocfilehash: bd55e2c061d8e99e0d9e9fd5d9be459b3daae524
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813325"
---
# <a name="bulletstring-cell-paragraph-section"></a>Ячейка BulletString (раздел "Абзац")

Позволяет создавать пользовательские стили маркеров. 
  
## <a name="remarks"></a>Замечания

Укажите стиль как строку (в кавычках). Например можно ввести строку «ООО».
  
Вы может также необходимо задать значение ячейки, щелкнув правой кнопкой мыши фигуру, с указанием **формате**, нажав кнопку **текст**и затем выбрав вкладку **маркеры** . 
  
Чтобы получить ссылку на ячейку BulletString по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |Para.BulletStr [ *i* ] где *i* = < 1 > 2, 3,...  <br/> |
   
Для получения ссылки на ячейки BulletString по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionParagraph** <br/> |
|Индекс строки:  <br/> |**visRowParagraph** +  *i* где *i* = 0, 1, 2,...  <br/> |
|Индекс ячейки:  <br/> |**visBulletString** <br/> |
   

