---
title: Overline Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251728
localization_priority: Normal
ms.assetid: 102cce17-43ee-e313-3412-a72d6ee18fe6
description: Определяет, есть ли над текстом строка.
ms.openlocfilehash: d5df39c2f12890d5fb4881346516abdb4f2b8099
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431647"
---
# <a name="overline-cell-character-section"></a>Overline Cell (Character Section)

Определяет, есть ли над текстом строка.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Над текстом есть строка.  <br/> |
|FALSE  <br/> |Текст не имеет строки над ней.  <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить значение этой ячейки с помощью диалогового окна **Text** (на вкладке **Главная** щелкните **стрелку Шрифта).** 
  
Чтобы получить ссылку на ячейку Overline по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Char.Overline[i] где *i* = <1>, 2.  3...  <br/> |
   
Чтобы получить ссылку на ячейку Overline по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionCharacter** <br/> |
|Индекс строки:  <br/> |**visRowCharacter**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
|Индекс ячейки:  <br/> |**visCharacterOverline** <br/> |
   

