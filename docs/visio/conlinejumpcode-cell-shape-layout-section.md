---
title: ConLineJumpCode Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251652
localization_priority: Normal
ms.assetid: af85588e-8e83-5168-7a8c-d7e8b4af5c27
description: Определяет, когда соединитатель скачет.
ms.openlocfilehash: 28bf506b8d3729fefec438d259746661fd28586e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421622"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a>ConLineJumpCode Cell (Shape Layout Section)

Определяет, когда соединитатель скачет.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Как указывает страница; На **вкладке Design** щелкните стрелку в группе **установки** страниц, а затем нажмите вкладку **Макет** и маршрутная маршрутная схема, чтобы увидеть спецификации страницы  <br/> |**visSLOJumpDefault** <br/> |
|1  <br/> |Никогда  <br/> |**visSLOJumpNever** <br/> |
|2  <br/> |Всегда  <br/> |**visSLOJumpAlways** <br/> |
|3  <br/> |Другие прыжки соединитетеля  <br/> |**visSLOJumpOther** <br/> |
|4   <br/> |Ни один из соединителеров не скачет  <br/> |**visSLOJumpNeither** <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить значение этой ячейки, выбрав динамический соединитель, щелкнув "Поведение" в группе **Shape Design** на вкладке Разработчик, а затем нажав вкладку **Соединитель.**  [](run-in-developer-mode-display-the-developer-tab.md) 
  
Чтобы получить ссылку на ячейку ConLineJumpCode по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |ConLineJumpCode  <br/> |
   
Чтобы получить ссылку на ячейку ConLineJumpCode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
|Индекс ячейки:  <br/> |**visSLOJumpCode** <br/> |
   

