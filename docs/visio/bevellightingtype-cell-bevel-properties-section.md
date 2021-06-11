---
title: BevelLightingType Cell (Bevel Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7fbb4b16-fe54-42d6-803a-c9980897166d
description: Определяет тип освещения, используемого эффектом bevel.
ms.openlocfilehash: 6d92c56b01d192c1df04eecdaca4eb915baebcae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433964"
---
# <a name="bevellightingtype-cell-bevel-properties-section"></a>BevelLightingType Cell (Bevel Properties Section)

Определяет тип освещения, используемого эффектом bevel.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Отсутствие освещения  <br/> |
|1  <br/> |Три точки  <br/> |
|2  <br/> |Баланс  <br/> |
|3  <br/> |Мягкий  <br/> |
|4   <br/> |Суровая  <br/> |
|5   <br/> |Наводнение  <br/> |
|6   <br/> |Контрастность  <br/> |
|7   <br/> |Утро  <br/> |
|8   <br/> |Восход солнца  <br/> |
|9   <br/> |Завершение  <br/> |
|10   <br/> |Chilly  <br/> |
|11  <br/> |Замораживание  <br/> |
|12   <br/> |Flat  <br/> |
|13  <br/> |Two Point  <br/> |
|14   <br/> |Подсветка  <br/> |
|15  <br/> |Bright Room  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на **ячейку BevelLightingType** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы с использованием свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |BevelLightingType  <br/> |
   
Чтобы получить ссылку на **ячейку BevelLightingType** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowBevelProperties** <br/> |
|Индекс ячейки:  <br/> |**visBevelLightingType** <br/> |
   

