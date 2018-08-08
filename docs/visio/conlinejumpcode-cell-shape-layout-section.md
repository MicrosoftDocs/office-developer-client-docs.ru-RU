---
title: Ячейка ConLineJumpCode (раздел "Макет фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251652
localization_priority: Normal
ms.assetid: af85588e-8e83-5168-7a8c-d7e8b4af5c27
description: Определяет, когда соединительные линии.
ms.openlocfilehash: 002f628841356ec8a22afbb9d4aeca8236058222
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813466"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a>Ячейка ConLineJumpCode (раздел "Макет фигуры")

Определяет, когда соединительные линии.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Как указано для страницы; на вкладке " **Конструктор** " щелкните стрелку в группе **Параметры страницы** и перейдите на вкладку **Макет и маршрутизации** , чтобы увидеть спецификации страниц  <br/> |**visSLOJumpDefault** <br/> |
|1  <br/> |Никогда не  <br/> |**visSLOJumpNever** <br/> |
|2  <br/> |Всегда  <br/> |**visSLOJumpAlways** <br/> |
|3  <br/> |Другие ссылки соединителя  <br/> |**visSLOJumpOther** <br/> |
|4  <br/> |Ни одна из соединительные линии  <br/> |**visSLOJumpNeither** <br/> |
   
## <a name="remarks"></a>Замечания

Можно также значение ячейки с выбор динамического соединителя, нажав кнопку **поведение** группы **Разработки фигуры** на вкладки " [Разработчик](run-in-developer-mode-display-the-developer-tab.md) " и затем выбрав вкладку **соединителя** . 
  
Чтобы получить ссылку на ячейку ConLineJumpCode по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |ConLineJumpCode  <br/> |
   
Для получения ссылки на ячейки ConLineJumpCode по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
|Индекс ячейки:  <br/> |**visSLOJumpCode** <br/> |
   

