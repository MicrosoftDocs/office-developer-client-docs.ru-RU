---
title: Функция HUE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251440
localization_priority: Normal
ms.assetid: 0f5c6097-eef5-5f58-e2ef-2c348e42dc9a
description: Возвращает значение компонента оттенка цвета.
ms.openlocfilehash: 39fdd160f5cd792e95930a3e7c7cea3c37ed16c1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439494"
---
# <a name="hue-function"></a>Функция HUE

Возвращает значение компонента оттенка цвета.
  
## <a name="syntax"></a>Синтаксис

HUE(** *выражение* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Обязательный  <br/> |**String** <br/> |Выражение, которое оценивается в цвет.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Номер
  
## <a name="remarks"></a>Примечания

Возвратное значение — это число в диапазоне от 0 до 239 включительно. Вход — это индекс цвета в цветовой таблице документа, выражение, которое решается на настраиваемый цвет (например, RGB или HSL), или ссылку на ячейку, содержаную цветной индекс или результат цвета. Функция возвращает 0 для недействительных входных данных. 
  
## <a name="example-1"></a>Пример 1

HUE(Sheet.4! FillForegnd)
  
Возвращает оттенок цвета переднего плана заполняемого листа.4.
  
## <a name="example-2"></a>Пример 2

HUE(7)
  
Возвращает 120, если в документе используется цветовая палитра Microsoft Visio microsoft, где cyan — это цвет в индексе 7.
  
## <a name="example-3"></a>Пример 3

HUE (HSL(10, 20, 30) )
  
Возвращает 10.
  

