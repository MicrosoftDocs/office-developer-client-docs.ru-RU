---
title: Ячейка XGridDensity (раздел "Линейка и сетка")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
localization_priority: Normal
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: Указывает тип горизонтальной сетки для использования.
ms.openlocfilehash: 107cde8e8b0d630a4dc4b43127412de2f6b0115d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815194"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a>Ячейка XGridDensity (раздел "Линейка и сетка")

Указывает тип горизонтальной сетки для использования.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Фиксация  <br/> |**visGridFixed** <br/> |
|2  <br/> |С большими интервалами  <br/> |**visGridCoarse** <br/> |
|4  <br/> |С обычными интервалами (по умолчанию)  <br/> |**visGridNormal** <br/> |
|8  <br/> |С небольшими интервалами  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>Замечания

Эта ячейка соответствует параметру **Интервал между линиями сетки по горизонтали** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**). 
  
Чтобы получить ссылку на ячейку XGridDensity по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |XGridDensity  <br/> |
   
Чтобы получить ссылку на ячейку XGridDensity по индексу из программы, укажите свойство **CellsSRC** с такими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowRulerGrid** <br/> |
|Индекс ячейки:  <br/> |**visXGridDensity** <br/> |
   

