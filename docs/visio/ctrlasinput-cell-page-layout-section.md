---
title: Ячейка CtrlAsInput (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1225
localization_priority: Normal
ms.assetid: c6fd0aba-7c33-b77f-207b-ba704b3e0756
description: Определяет, какие фигуры родительский при использовании фигур с помощью маркеров элемента управления. В этой ячейке указывается, что для всех фигур на странице документа.
ms.openlocfilehash: a87ba7451d73af50de4a110ecdc12b3e23e14d5d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813518"
---
# <a name="ctrlasinput-cell-page-layout-section"></a>Ячейка CtrlAsInput (раздел "Макет страницы")

Определяет, какие фигуры родительский при использовании фигур с помощью маркеров элемента управления. В этой ячейке указывается, что для всех фигур на странице документа.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Задайте фигуры, подключенной к дескриптора элемента управления в качестве родительского.  <br/> |
| FALSE  <br/> | По умолчанию. Набор фигуры, содержащее дескриптор управления как родительский элемент.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку CtrlAsInput по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | CtrlAsInput  <br/> |
   
Для получения ссылки на ячейки CtrlAsInput по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPageLayout** <br/> |
| Индекс ячейки:  <br/> |**visPLOCtrlAsInput** <br/> |
   

