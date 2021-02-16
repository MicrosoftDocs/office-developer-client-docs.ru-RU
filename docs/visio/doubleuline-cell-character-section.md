---
title: DoubleULine Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm260
localization_priority: Normal
ms.assetid: c18955c8-d653-c29d-d3da-9d3cd0241e17
description: Определяет, имеет ли диапазон текста двойной подчеркнутой под ней.
ms.openlocfilehash: 2708e7f55e1fd04d5fb902b3d382035790cbbcc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438843"
---
# <a name="doubleuline-cell-character-section"></a>DoubleULine Cell (Character Section)

Определяет, имеет ли диапазон текста двойной подчеркнутой под ней.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Под текстом есть двойное подчеркнути.  <br/> |
|FALSE  <br/> |Под текстом нет двойного подчеркнутия.  <br/> |
   
## <a name="remarks"></a>Примечания

Ячейка DoubleULine содержит сведения о форматированиях, применяемые к под диапазону текста фигуры, если раздел Characters содержит несколько строк. В противном случае он содержит сведения о формате для всего текста фигуры.
  
Значение этой ячейки также можно установить с помощью диалогового  окна **"Текст"** (щелкните стрелку шрифта на вкладке **"Главная").** 
  
Чтобы получить ссылку на ячейку DoubleULine по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Char.DblUnderline[ *i*  ] где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку DoubleULine по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionCharacter** <br/> |
|Индекс строки:  <br/> |**visRowCharacter**  +   *i* где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visCharacterDblUnderline** <br/> |
   

