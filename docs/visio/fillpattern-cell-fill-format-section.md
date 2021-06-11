---
title: FillPattern Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm375
localization_priority: Normal
ms.assetid: dac82a4f-4508-541a-e118-7d79df987232
description: Определяет шаблон заполнения фигуры. Чтобы указать настраиваемый шаблон заполнения, используйте функцию USE в этой ячейке.
ms.openlocfilehash: 340ccdc9f3819fb29e210832107e270bd302433c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422931"
---
# <a name="fillpattern-cell-fill-format-section"></a>FillPattern Cell (Fill Format Section)

Определяет шаблон заполнения фигуры. Чтобы указать настраиваемый шаблон заполнения, используйте функцию USE в этой ячейке.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Нет (прозрачное заполнение).  <br/> |
|1  <br/> |Сплошной цвет переднего плана.  <br/> |
|2 - 40  <br/> |Различные шаблоны заполнения, соответствующие индексным записям в диалоговом окне **Fill.**  <br/> |
   
## <a name="remarks"></a>Примечания

Это значение также можно установить в диалоговом окне **Fill** (на вкладке **Главная,** в группе **Shape,** щелкните **Заполните** и нажмите **кнопку Параметры заполнения).**
  
Чтобы получить ссылку на ячейку FillPattern по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |FillPattern  <br/> |
   
Чтобы получить ссылку на ячейку FillPattern по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowFill** <br/> |
|Индекс ячейки:  <br/> |**visFillPattern** <br/> |
   

