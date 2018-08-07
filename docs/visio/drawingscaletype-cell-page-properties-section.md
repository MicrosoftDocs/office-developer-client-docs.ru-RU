---
title: Ячейка DrawingScaleType (раздел "Свойства страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm270
localization_priority: Normal
ms.assetid: 5d4f1cf8-bc1f-07b8-1da5-7253808e337e
description: Определяет масштаб документа, указанный в диалоговом окне Параметры страницы (щелкните стрелку Параметры страницы на вкладке "Главная").
ms.openlocfilehash: b93bd95a30fe5a8a5de15a8e5ea104279cf1bcda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813662"
---
# <a name="drawingscaletype-cell-page-properties-section"></a>Ячейка DrawingScaleType (раздел "Свойства страницы")

Определяет масштаб документа, указанный в диалоговом окне **Параметры страницы** (щелкните стрелку **Параметры страницы** на вкладке **Главная** ). 
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Нет масштаба  <br/> |**visNoScale** <br/> |
| 1  <br/> | Архитектурные масштаба  <br/> |**visArchitectural** <br/> |
| 2  <br/> | Масштаб Гражданское Engineering  <br/> |**visEngineering** <br/> |
| 3  <br/> | Настраиваемые масштаба  <br/> |**visScaleCustom** <br/> |
| 4  <br/> | Метрики  <br/> |**visScaleMetric** <br/> |
| 5  <br/> | Схема Engineering масштаба  <br/> |**visScaleMechanical** <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку DrawingScaleType по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | DrawingScaleType  <br/> |
   
Для получения ссылки на ячейки DrawingScaleType по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPage** <br/> |
| Индекс ячейки:  <br/> |**visPageDrawScaleType** <br/> |
   

