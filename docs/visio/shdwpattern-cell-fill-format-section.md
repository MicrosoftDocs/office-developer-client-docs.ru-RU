---
title: ShdwPattern Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm935
localization_priority: Normal
ms.assetid: eca73b80-9835-9011-1dce-187ccee92e76
description: Определяет шаблон заливки для тени фигуры.
ms.openlocfilehash: c2591fbc9f208b1bf9c7d0c85e6de765cd9825f6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427614"
---
# <a name="shdwpattern-cell-fill-format-section"></a>ShdwPattern Cell (Fill Format Section)

Определяет шаблон заливки для тени фигуры.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Нет (прозрачная заливка)  <br/> |
|1   <br/> |Сплошной цвет переднего плана  <br/> |
|2 - 40  <br/> |Различные шаблоны  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы установить шаблон заливки, введите число от 0 до 40, которое является индексом в коллекцию шаблонов. Вы можете просмотреть коллекцию  шаблонов заливки  в диалоговом окне "Заливка" (на вкладке "Главная" в группе "Фигура" щелкните "Заполнить" и выберите **"Параметры заливки").** 
  
Чтобы получить ссылку на ячейку ShdwPattern по имени из другой формулы или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |ShdwPattern  <br/> |
   
Чтобы получить ссылку на ячейку ShdwPattern по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowFill** <br/> |
|Индекс ячейки:  <br/> |**visFillShdwPattern** <br/> |
   

