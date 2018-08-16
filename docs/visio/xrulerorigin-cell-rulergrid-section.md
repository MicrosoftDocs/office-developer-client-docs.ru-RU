---
title: Ячейка XRulerOrigin (раздел "Линейка и сетка")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1170
localization_priority: Normal
ms.assetid: 328f8ab5-217f-0336-0d56-611eff509fe8
description: Указывает точку начала координат на линейке по оси X для страницы.
ms.openlocfilehash: 78fab70c8489ddcdfe450ef9f9fd88b6c5040211
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815200"
---
# <a name="xrulerorigin-cell-ruler-amp-grid-section"></a>Ячейка XRulerOrigin (раздел "Линейка и сетка")

Указывает точку начала координат на линейке по оси X для страницы.
  
## <a name="remarks"></a>Замечания

Эта ячейка соответствует параметру **Ноль на горизонтальной линейке** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**). 
  
Чтобы получить ссылку на ячейку XRulerOrigin по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |XRulerOrigin  <br/> |
   
Чтобы получить ссылку на ячейку XRulerOrigin по индексу из программы, укажите свойство **CellsSRC** с такими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowRulerGrid** <br/> |
|Индекс ячейки:  <br/> |**visXRulerOrigin** <br/> |
   

