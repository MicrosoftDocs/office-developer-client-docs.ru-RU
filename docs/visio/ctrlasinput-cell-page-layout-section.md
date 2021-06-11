---
title: CtrlAsInput Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1225
localization_priority: Normal
ms.assetid: c6fd0aba-7c33-b77f-207b-ba704b3e0756
description: Определяет, какая форма является родительской при использовании фигур с ручками управления. Эта ячейка задает поведение для всех фигур на странице рисования.
ms.openlocfilehash: a530c48156043bec0cd58d79aead1a403c17ddce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422623"
---
# <a name="ctrlasinput-cell-page-layout-section"></a>CtrlAsInput Cell (Page Layout Section)

Определяет, какая форма является родительской при использовании фигур с ручками управления. Эта ячейка задает поведение для всех фигур на странице рисования.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Установите фигуру, к которую подключена ручка управления как родитель.  <br/> |
| FALSE  <br/> | По умолчанию. Установите фигуру, содержаную ручку управления в качестве родительского.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку CtrlAsInput по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | CtrlAsInput  <br/> |
   
Чтобы получить ссылку на ячейку CtrlAsInput по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPageLayout** <br/> |
| Индекс ячейки:  <br/> |**visPLOCtrlAsInput** <br/> |
   

