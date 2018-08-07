---
title: Ячейка CenterX (раздел "Свойства печати")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60030
localization_priority: Normal
ms.assetid: 890e2537-66a5-2863-c78d-320b42565ea7
description: Определяет, будет ли страницы рисунка центру по по горизонтали на странице принтера.
ms.openlocfilehash: a12b60f7d183a27d938bd18a1f571ef01af455d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813378"
---
# <a name="centerx-cell-print-properties-section"></a>Ячейка CenterX (раздел "Свойства печати")

Определяет, будет ли страницы рисунка центру по по горизонтали на странице принтера. 
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Центр страницы рисунка по горизонтали на странице принтера.  <br/> |
| FALSE  <br/> | Не центрирования страницы рисунка по горизонтали на странице принтера (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Замечания

По умолчанию страниц документа краю верхней и левой части страницы принтера. Установка ячейки CenterX и CenterY TRUE местах на странице документа в центре страницы принтера (или страниц при необходимости заполнения). 
  
Чтобы получить ссылку на ячейку CenterX по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | CenterX  <br/> |
   
Для получения ссылки на ячейки CenterX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPrintProperties** <br/> |
| Индекс ячейки:  <br/> |**visPrintPropertiesCenterX** <br/> |
   

