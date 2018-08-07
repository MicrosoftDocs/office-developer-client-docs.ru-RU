---
title: Ячейка DrawingSizeType (раздел "Свойства страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm275
localization_priority: Normal
ms.assetid: 7fe270e8-0dff-bf1f-dfc0-c0608af79f59
description: Определяет размер документа.
ms.openlocfilehash: a87f37ac79d00aeb064072389db432421b33d2d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813650"
---
# <a name="drawingsizetype-cell-page-properties-section"></a>Ячейка DrawingSizeType (раздел "Свойства страницы")

Определяет размер документа.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |То же, что принтера  <br/> |**visPrintSetup** <br/> |
|1  <br/> |Вписать страницу в содержимое документа  <br/> |**visTight** <br/> |
|2  <br/> |Standard  <br/> |**visStandard** <br/> |
|3  <br/> |Пользовательский размер страницы  <br/> |**visCustom** <br/> |
|4  <br/> |Настраиваемые масштабируемая размер рисунка  <br/> |**visLogical** <br/> |
|5  <br/> |Показатель (ISO)  <br/> |**visDSMetric** <br/> |
|6  <br/> |Инженерные работы по ANSI  <br/> |**visDSEngr** <br/> |
|7  <br/> |Архитектурные ANSI  <br/> |**visDSArch** <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы задать размер рисунка, используйте диалоговое окно " **Параметры страницы** " (щелкните стрелку **Параметры страницы** на вкладке **Конструктор** ) или вручную изменить размер страницы с помощью мыши. 
  
Чтобы получить ссылку на ячейку DrawingSizeType по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |DrawingSizeType  <br/> |
   
Для получения ссылки на ячейки DrawingSizeType по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPage** <br/> |
|Индекс ячейки:  <br/> |**visPageDrawSizeType** <br/> |
   

