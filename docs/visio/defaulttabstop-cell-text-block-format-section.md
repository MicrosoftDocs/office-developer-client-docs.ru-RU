---
title: DefaultTabstop Cell (Text Block Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm220
localization_priority: Normal
ms.assetid: 3b3e458a-206c-8699-8bf7-da80f4350706
description: Определяет интервал остановки вкладки по умолчанию в текстовом блоке.
ms.openlocfilehash: 1ae923f6373b9cee76238b1fb27ec5eb3acb43ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407832"
---
# <a name="defaulttabstop-cell-text-block-format-section"></a>DefaultTabstop Cell (Text Block Format Section)

Определяет интервал остановки вкладки по умолчанию в текстовом блоке. 
  
## <a name="remarks"></a>Примечания

Значение по умолчанию — 0,5 дюйма для документов, созданных в единицах измерения, и 1,5 дюйма для документов, созданных в единицах измерения.
  
Чтобы получить ссылку на ячейку DefaultTabstop по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |DefaultTabstop  <br/> |
   
Чтобы получить ссылку на ячейку DefaultTabstop по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowText** <br/> |
|Индекс ячейки:  <br/> |**visTxtBlkDefaultTabStop** <br/> |
   

