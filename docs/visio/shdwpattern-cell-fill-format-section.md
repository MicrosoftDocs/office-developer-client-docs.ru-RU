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
description: Определяет узор заливки для тени фигуры.
ms.openlocfilehash: c2591fbc9f208b1bf9c7d0c85e6de765cd9825f6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349044"
---
# <a name="shdwpattern-cell-fill-format-section"></a>ShdwPattern Cell (Fill Format Section)

Определяет узор заливки для тени фигуры.
  
|**Value**|**Описание**|
|:-----|:-----|
|нуль  <br/> |Нет (прозрачная заливка)  <br/> |
|1,1  <br/> |Сплошной цвет переднего плана  <br/> |
|2-40  <br/> |Шаблоны ассортимента  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы задать шаблон Fill, введите число от 0 до 40, которое представляет собой индекс в коллекции шаблонов. Вы можете просмотреть коллекцию шаблонов заливки в диалоговом окне **Заливка** (на вкладке **Главная** , в группе **фигур** нажмите кнопку **Заливка**, а затем выберите команду **Параметры заливки**).
  
Чтобы получить ссылку на ячейку ShdwPattern по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |ShdwPattern  <br/> |
   
Чтобы получить ссылку на ячейку ShdwPattern по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**Висровфилл** <br/> |
|Индекс ячейки:  <br/> |**Висфиллшдвпаттерн** <br/> |
   

