---
title: Ячейка DefaultTabstop (раздел "Формат текстового блока")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm220
localization_priority: Normal
ms.assetid: 3b3e458a-206c-8699-8bf7-da80f4350706
description: Задает интервал табуляции по умолчанию в блоке текста.
ms.openlocfilehash: 2b9c2c5b03da98b30e338a250b56091479067955
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813591"
---
# <a name="defaulttabstop-cell-text-block-format-section"></a>Ячейка DefaultTabstop (раздел "Формат текстового блока")

Задает интервал табуляции по умолчанию в блоке текста. 
  
## <a name="remarks"></a>Замечания

Значение по умолчанию — 0,5 дюйма для документов, созданных в Британская и 1,5 см для документов, созданных в метрическая система мер.
  
Чтобы получить ссылку на ячейку DefaultTabstop по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |DefaultTabstop  <br/> |
   
Для получения ссылки на ячейки DefaultTabstop по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowText** <br/> |
|Индекс ячейки:  <br/> |**visTxtBlkDefaultTabStop** <br/> |
   

