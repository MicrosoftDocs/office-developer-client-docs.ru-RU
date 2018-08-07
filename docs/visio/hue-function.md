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
description: Возвращает значение компонента тона цвета.
ms.openlocfilehash: 2a532e305eb7cbabc5ba07dcace6c07a337e7743
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813919"
---
# <a name="hue-function"></a>Функция HUE

Возвращает значение компонента тона цвета.
  
## <a name="syntax"></a>Синтаксис

ТОНА (** *выражение* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Обязательный  <br/> |**Строка** <br/> |Выражение, которое оценивается как цвет.  <br/> |
   
### <a name="return-value"></a>������������ ��������

Number
  
## <a name="remarks"></a>Замечания

Возвращаемое значение — число в диапазоне 0 для 239 включительно. Входные данные является индекс цвета в таблице цветов документа, выражение, которое разрешается в настраиваемый цвет (например, RGB или HSL) или ссылка на ячейку, которая содержит индекс цвета или цвет результатов. Функция возвращает 0 для недопустимые данные. 
  
## <a name="example-1"></a>Пример 1

ТОНА (Sheet.4! FillForegnd)
  
Возвращает цветовым цвет заливки Sheet. 4.
  
## <a name="example-2"></a>Пример 2

HUE(7)
  
Возвращает 120, если в документе используется по умолчанию Microsoft Visio цветовой палитры, в котором голубой цвет по индексу 7.
  
## <a name="example-3"></a>Пример 3

ТОНА (HSL (10, 20, 30))
  
Возвращает значение 10.
  

