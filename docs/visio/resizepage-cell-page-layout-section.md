---
title: ResizePage Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm850
localization_priority: Normal
ms.assetid: d63fe874-1027-3436-dbc1-73e722bce22e
description: Определяет, следует ли увеличивать страницу, чтобы заключить рисунок после сложения фигур, с помощью диалоговых окна "Настройка макета" (на вкладке "Конструктор" в группе "Макет" щелкните Re-Layout", а затем щелкните "Дополнительные параметры макета").
ms.openlocfilehash: 8d0001ce35808f8c5f11068ed78865ce992af5cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438094"
---
# <a name="resizepage-cell-page-layout-section"></a>ResizePage Cell (Page Layout Section)

Определяет, следует ли увеличивать страницу, чтобы заключить рисунок после выкладки фигур, используя диалоговое  окно "Настройка  макета" (на вкладке "Конструктор" в группе "Макет" щелкните "Страница повторного макета", а затем щелкните "Дополнительные параметры   макета"). 
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Увеличение страницы.  <br/> |
| FALSE  <br/> | Не увеличивать страницу.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку ResizePage по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | ResizePage  <br/> |
   
Чтобы получить ссылку на ячейку ResizePage по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPageLayout** <br/> |
| Индекс ячейки:  <br/> |**visPLOResizePage** <br/> |
   

