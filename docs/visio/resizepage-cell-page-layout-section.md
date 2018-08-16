---
title: Ячейка ResizePage (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm850
localization_priority: Normal
ms.assetid: d63fe874-1027-3436-dbc1-73e722bce22e
description: Определяет, следует ли увеличить страницу для помещения документа после расположения фигур с помощью диалогового окна "Настройка макета" (на вкладке конструктор в группе макет нажмите кнопку Изменить расположение и нажмите кнопку Дополнительные параметры расположения).
ms.openlocfilehash: fab37ee4561ba82ea1f314ad595e513253478b30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814607"
---
# <a name="resizepage-cell-page-layout-section"></a>Ячейка ResizePage (раздел "Макет страницы")

Определяет, следует ли увеличить страницу для помещения документа после расположения фигур с помощью диалогового окна " **Настройка макета** " (на вкладке **Конструктор** в группе **Макет** нажмите кнопку **Изменить** расположение и нажмите кнопку **более макета Параметры**).
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Увеличьте страницу.  <br/> |
| FALSE  <br/> | Не увеличить страницу.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку ResizePage по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | ResizePage  <br/> |
   
Для получения ссылки на ячейки ResizePage по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPageLayout** <br/> |
| Индекс ячейки:  <br/> |**visPLOResizePage** <br/> |
   
