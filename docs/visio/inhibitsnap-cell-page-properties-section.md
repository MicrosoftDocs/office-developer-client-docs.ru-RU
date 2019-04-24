---
title: InhibitSnap Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251620
localization_priority: Normal
ms.assetid: ab9fcebc-1550-3b9e-e3b4-e8b92424390b
description: Определяет, привязываются ли фигуры на переднем плане к другим объектам на странице и фигурам на фоновой странице.
ms.openlocfilehash: 665130e9f9f938349028ffa1d1c06224e746de5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335324"
---
# <a name="inhibitsnap-cell-page-properties-section"></a>InhibitSnap Cell (Page Properties Section)

Определяет, привязываются ли фигуры на переднем плане к другим объектам на странице и фигурам на фоновой странице.
  
|**Value**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Запрет на все привязки на странице, за исключением привязки к линейке и сетке.  <br/> |
| FALSE  <br/> | Включить привязку.  <br/> |
   
## <a name="remarks"></a>Комментарии

Чтобы получить ссылку на ячейку InhibitSnap по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | InhibitSnap  <br/> |
   
Чтобы получить ссылку на ячейку InhibitSnap по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровпаже** <br/> |
| Индекс ячейки:  <br/> |**Виспажеинхибитснап** <br/> |
   

