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
description: Определяет, будут ли фигуры на странице переднего плана прикреплены к другим объектам на странице и фигурам на фоновой странице.
ms.openlocfilehash: 665130e9f9f938349028ffa1d1c06224e746de5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426753"
---
# <a name="inhibitsnap-cell-page-properties-section"></a>InhibitSnap Cell (Page Properties Section)

Определяет, будут ли фигуры на странице переднего плана прикреплены к другим объектам на странице и фигурам на фоновой странице.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Блокирование всех прикреплений на странице, кроме прикрепления к линейке и сетке.  <br/> |
| FALSE  <br/> | Включить прикрепление.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку InhibitSnap по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | InhibitSnap  <br/> |
   
Чтобы получить ссылку на ячейку InhibitSnap по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPage** <br/> |
| Индекс ячейки:  <br/> |**visPageInhibitSnap** <br/> |
   

