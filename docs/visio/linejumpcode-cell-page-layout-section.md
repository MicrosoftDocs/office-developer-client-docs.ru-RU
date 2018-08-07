---
title: Ячейка LineJumpCode (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm540
localization_priority: Normal
ms.assetid: 56f9043d-a632-65df-c710-45867cce1627
description: Определяет соединители, к которым требуется добавить переходы.
ms.openlocfilehash: abb7208c2cfbd6b1423e091efc1d526f8b10b57d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814075"
---
# <a name="linejumpcode-cell-page-layout-section"></a>Ячейка LineJumpCode (раздел "Макет страницы")

Определяет соединители, к которым требуется добавить переходы.
  
|**Значение**|**Соединители, к которым требуется добавить переходы**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Нет  <br/> |**visPLOJumpNone** <br/> |
|1  <br/> |Горизонтальные линии  <br/> |**visPLOJumpHorizontal** <br/> |
|2  <br/> |Вертикальные линии  <br/> |**visPLOJumpVertical** <br/> |
|3  <br/> |Последняя строка маршрутизации  <br/> |**visPLOJumpLastRouted** <br/> |
|4  <br/> |Предыдущей строки (Основные фигуры в *z* -порядке)  <br/> |**visPLOJumpDisplayOrder** <br/> |
|5  <br/> |Сначала отображается строка (фигуры в нижней части *z* -порядке)  <br/> |**visPLOJumpReverseDisplayOrder** <br/> |
   
## <a name="remarks"></a>Замечания

Значение ячейки также можно настроить на вкладке **Макет и маршрутизации** в диалоговом окне " **Параметры страницы** " (на вкладки " **Конструктор** ", нажмите кнопку со стрелкой **Параметры страницы** и нажмите кнопку **Макет и маршрутизации**).
  
Чтобы получить ссылку на ячейку LineJumpCode по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |LineJumpCode  <br/> |
   
Для получения ссылки на ячейки LineJumpCode по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPageLayout** <br/> |
|Индекс ячейки:  <br/> |**visPLOJumpCode** <br/> |
   

