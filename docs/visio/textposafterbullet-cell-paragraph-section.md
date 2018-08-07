---
title: Ячейка TextPosAfterBullet (раздел "Абзац")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60089
localization_priority: Normal
ms.assetid: 08958abb-9d66-5a83-dac3-4cbfd1f6d85e
description: Представляет расстояние между первой строкой абзаца и маркером.
ms.openlocfilehash: fe22b81113ab6537922ad4627aa53f34f2e62c48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815008"
---
# <a name="textposafterbullet-cell-paragraph-section"></a>Ячейка TextPosAfterBullet (раздел "Абзац")

Представляет расстояние между первой строкой абзаца и маркером. 
  
## <a name="remarks"></a>Замечания

Это расстояние добавляется расстояние, содержащихся в ячейке IndFirst, который является отступа по умолчанию. Это значение не зависит от масштаба документа. 
  
Чтобы получить ссылку на ячейку TextPosAfterBullet по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Para.TextPosAfterBullet [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки TextPosAfterBullet по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionParagraph** <br/> |
| Индекс строки:  <br/> |**visRowParagraph** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visTextPosAfterBullet** <br/> |
   

