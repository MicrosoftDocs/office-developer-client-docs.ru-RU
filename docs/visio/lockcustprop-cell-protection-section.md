---
title: LockCustProp Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60055
localization_priority: Normal
ms.assetid: d1c23f1d-485d-a897-594d-15d6e8d0fb3c
description: Определяет, может ли пользователь добавлять, удалять или изменять данные фигуры в пользовательском интерфейсе (пользовательском интерфейсе) с помощью диалогового окна Define Shape Data или меню ярлыка для окна Данных формы.
ms.openlocfilehash: 001123f3bd08d35f6f8e4874e20f2ee073835494
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422525"
---
# <a name="lockcustprop-cell-protection-section"></a>LockCustProp Cell (Protection Section)

Определяет, может ли пользователь добавлять, удалять или изменять данные фигуры в пользовательском интерфейсе (пользовательском интерфейсе) с помощью диалогового окна **Define Shape Data** или меню ярлыка для окна Данных **формы.** 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Отключена команда **Define Shape Data** в меню ярлыков в окне Shape **Data.**  <br/> |
|FALSE  <br/> |Включена **команда Define Shape Data** в меню ярлыка в окне Shape **Data** (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Примечания

Значение TRUE не мешает пользователю изменять значение элемента данных фигуры или изменять раздел Shape Data в окне ShapeSheet. 
  
Чтобы получить ссылку на ячейку LockCustProp по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |LockCustProp  <br/> |
   
Чтобы получить ссылку на ячейку LockCustProp по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowLock** <br/> |
|Индекс ячейки:  <br/> |**visLockCustProp** <br/> |
   

