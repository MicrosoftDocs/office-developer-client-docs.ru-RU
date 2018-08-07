---
title: Ячейка ShdwPattern (раздел "Формат заливки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm935
localization_priority: Normal
ms.assetid: eca73b80-9835-9011-1dce-187ccee92e76
description: Определяет узор заливки для тени фигуры.
ms.openlocfilehash: fd24a8d23d62436a6d81cf6b8049dcabe47db677
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814832"
---
# <a name="shdwpattern-cell-fill-format-section"></a>Ячейка ShdwPattern (раздел "Формат заливки")

Определяет узор заливки для тени фигуры.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |None (прозрачной заливки)  <br/> |
|1  <br/> |Сплошной цвет  <br/> |
|2 - 40  <br/> |В этой модели  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы задать шаблон заполнения, введите число от 0 до 40, которая является индексом в коллекции шаблонов. Шаблон заполнения коллекции можно просмотреть в диалоговом окне **заливки** (на вкладке **Главная** в группе **фигуры** щелкните **заливки**и выберите пункт **Параметры заливки**).
  
Чтобы получить ссылку на ячейку ShdwPattern по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |ShdwPattern  <br/> |
   
Для получения ссылки на ячейки ShdwPattern по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowFill** <br/> |
|Индекс ячейки:  <br/> |**visFillShdwPattern** <br/> |
   

