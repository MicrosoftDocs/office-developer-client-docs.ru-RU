---
title: ConFixedCode Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm175
localization_priority: Normal
ms.assetid: 8e7c9080-7ef1-0696-a3d2-d8f57ea5ab9b
description: Определяет, когда соединителю перенапределяется.
ms.openlocfilehash: b2b9cde309c720493f0e46962b2fe6c2e79545d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404185"
---
# <a name="confixedcode-cell-shape-layout-section"></a>ConFixedCode Cell (Shape Layout Section)

Определяет, когда соединителю перенапределяется.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Перенастройка свободно  <br/> |**visSLOConFixedRerouteFreely** <br/> |
|1  <br/> |Перенастройка по мере необходимости (ручная перенастройка)  <br/> |**visSLOConFixedRerouteAsNeeded** <br/> |
|2  <br/> |Никогда не перенастройка  <br/> |**visSLOConFixedRerouteNever** <br/> |
|3  <br/> |Перенастройка на кроссовере  <br/> |**visSLOConFixedRerouteOnCrossover** <br/> |
|4   <br/> |Только для внутреннего использования  <br/> |**visSLOConFixedByAlgFrom** <br/> |
|5   <br/> |Только для внутреннего использования  <br/> |**visSLOConFixedByAlgTo** <br/> |
|6   <br/> |Только для внутреннего использования  <br/> |**visSLOConFixedByAlgFromTo** <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить значение этой ячейки, выбрав динамический соединитель, щелкнув "Поведение" в группе **Shape Design** на вкладке Разработчик, а затем нажав вкладку **Соединитель.**  [](run-in-developer-mode-display-the-developer-tab.md) 
  
Чтобы получить ссылку на ячейку ConFixedCode по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |ConFixedCode  <br/> |
   
Чтобы получить ссылку на ячейку ConFixedCode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
|Индекс ячейки:  <br/> |**visSLOConFixedCode** <br/> |
   

