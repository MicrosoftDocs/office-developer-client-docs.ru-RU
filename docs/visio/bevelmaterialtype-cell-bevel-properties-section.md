---
title: BevelMaterialType Cell (Bevel Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 30f50a94-88dc-41a3-bb46-45c92d6817a4
description: Определяет тип материала, из которого состоит bevel.
ms.openlocfilehash: b8efaa1f84594c803c79be02cd88dda1a5346dc7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414587"
---
# <a name="bevelmaterialtype-cell-bevel-properties-section"></a>BevelMaterialType Cell (Bevel Properties Section)

Определяет тип материала, из которого состоит bevel. 
  
|**Описание**|**Значение**|
|:-----|:-----|
|0  <br/> |Нет специального материала  <br/> |
|1  <br/> |Matte  <br/> |
|2  <br/> |Warm Matte  <br/> |
|3  <br/> |Пластик  <br/> |
|4   <br/> |Metal  <br/> |
|5   <br/> |Dark Edge  <br/> |
|6   <br/> |Soft Edge  <br/> |
|7   <br/> |Flat  <br/> |
|8   <br/> |Wireframe  <br/> |
|9   <br/> |Powder  <br/> |
|10   <br/> |Полупрозрачный порошок  <br/> |
|11  <br/> |Очистка  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **BevelMaterialType** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы с использованием свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | BevelMaterialType  <br/> |
   
Чтобы получить ссылку на **ячейку BevelMaterialType** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowBevelProperties** <br/> |
| Индекс ячейки:  <br/> |**visBevelMaterialType** <br/> |
   

