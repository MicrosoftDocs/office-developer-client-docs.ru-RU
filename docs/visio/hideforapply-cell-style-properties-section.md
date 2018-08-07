---
title: Ячейка HideForApply (раздел "Свойства стиля")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251698
localization_priority: Normal
ms.assetid: 62d87db9-b8ca-60b6-bf27-5168c718ec96
description: Определяет, где стиля отображается в интерфейсе пользователя Microsoft Visio.
ms.openlocfilehash: 5b0221c54c17a3b9957cce5e890842def0ba7525
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813918"
---
# <a name="hideforapply-cell-style-properties-section"></a>Ячейка HideForApply (раздел "Свойства стиля")

Определяет, где стиля отображается в интерфейсе пользователя Microsoft Visio.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Показать стиль только в **Обозревателе документа**.  <br/> |
| FALSE  <br/> | Показать стиль в **Обозревателе документа**.  <br/> |
   
## <a name="remarks"></a>Замечания

Если новый стиль основывается на стиль, который скрыт, новый стиль не наследует этот атрибут.
  
Чтобы получить ссылку на ячейку HideForApply по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | HideForApply  <br/> |
   
Для получения ссылки на ячейки HideForApply по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowStyle** <br/> |
| Индекс ячейки:  <br/> |**visStyleHidden** <br/> |
   

