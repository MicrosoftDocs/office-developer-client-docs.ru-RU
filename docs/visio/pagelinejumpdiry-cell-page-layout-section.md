---
title: Ячейка PageLineJumpDirY (раздел макет страницы)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm770
localization_priority: Normal
ms.assetid: f73cc157-b332-279b-f7cf-d5a090bc09a4
description: Определяет направление строки пересечения на вертикальной динамической соединители на странице документа, для которого не применяются локальные направление.
ms.openlocfilehash: 640ad93fbccf2cec26bda535c288c881aea32207
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814349"
---
# <a name="pagelinejumpdiry-cell-page-layout-section"></a>Ячейка PageLineJumpDirY (раздел макет страницы)

Определяет направление строки пересечения на вертикальной динамической соединители на странице документа, для которого не применяются локальные направление.
  
|**Значение**|**Направление**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | По умолчанию; вверх или параметров страницы для фигур  <br/> |**visLOJumpDirYDefault** <br/> |
| 1  <br/> | Слева  <br/> |**visLOJumpDirYLeft** <br/> |
| 2  <br/> | Правильно  <br/> |**visLOJumpDirYRight** <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку PageLineJumpDirY по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | PageLineJumpDirY  <br/> |
   
Для получения ссылки на ячейки PageLineJumpDirY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPageLayout** <br/> |
| Индекс ячейки:  <br/> |**visPLOJumpDirY** <br/> |
   

