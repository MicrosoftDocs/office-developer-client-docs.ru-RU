---
title: Ячейка NoLiveDynamics (раздел "Прочее")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm720
localization_priority: Normal
ms.assetid: d1c4b9d9-6d64-8ed1-9fc6-2dbf829a75b5
description: Определяет фигуры динамически изменяет размер или поворот при работе с ней.
ms.openlocfilehash: 043571243fe3698561bee8632e7fd18db04c9330
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814297"
---
# <a name="nolivedynamics-cell-miscellaneous-section"></a>Ячейка NoLiveDynamics (раздел "Прочее")

Определяет фигуры динамически изменяет размер или поворот при работе с ней.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Не обновляются динамически фигуры во время при работе с ней.  <br/> |
| FALSE  <br/> | Динамическое обновление фигуры во время при работе с ней.  <br/> |
   
## <a name="remarks"></a>Замечания

Как изменить размер или поворот двухмерных фигуры (2-D) без динамическое обновление появится прямоугольник выделения. Если имеет одномерный (1-D), визуально основано на значения ячейки DynFeedback.
  
Чтобы получить ссылку на ячейку NoLiveDynamics по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | NoLiveDynamics  <br/> |
   
Для получения ссылки на ячейки NoLiveDynamics по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowMisc** <br/> |
| Индекс ячейки:  <br/> |**visNoLiveDynamics** <br/> |
   

