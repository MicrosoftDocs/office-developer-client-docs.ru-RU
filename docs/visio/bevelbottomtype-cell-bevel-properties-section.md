---
title: BevelBottomType Cell (Bevel Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ac7b39d4-3942-4b23-b188-2c3f69e54929
description: Указывает нижний тип bevel фигуры.
ms.openlocfilehash: 0cd360f633145c7dea95438ffe2bc746e519ce13
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431752"
---
# <a name="bevelbottomtype-cell-bevel-properties-section"></a>BevelBottomType Cell (Bevel Properties Section)

Указывает нижний тип bevel фигуры.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Без bevel  <br/> |
|1  <br/> |Круг bevel  <br/> |
|2  <br/> |Relaxed Inset bevel  <br/> |
|3  <br/> |Cross bevel  <br/> |
|4   <br/> |Cool Slant bevel  <br/> |
|5   <br/> |Угловая гоголевка  <br/> |
|6   <br/> |Soft Round bevel  <br/> |
|7   <br/> |Выпукшная гоголевка  <br/> |
|8   <br/> |Спусковая пусковая дорожка  <br/> |
|9   <br/> |Divot bevel  <br/> |
|10   <br/> |Риблет-букель  <br/> |
|11  <br/> |Hard Edge bevel  <br/> |
|12   <br/> |Ар-деко bevel  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **BevelBottomType** по имени из другой формулы, по значению атрибута **N** элемента **Cell** в формате файла .vsdx или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | BevelBottomType  <br/> |
   
Чтобы получить ссылку на ячейку **BevelBottomType** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowBevelProperties** <br/> |
| Индекс ячейки:  <br/> |**visBevelBottomType** <br/> |
   

