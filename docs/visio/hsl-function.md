---
title: Функция HSL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251438
localization_priority: Normal
ms.assetid: c9314c39-1d2e-a18f-c01b-8817286099dc
description: Возвращает значение, представляющее индекс в цветовой палитре документа. Он указывает цвет по своему оттенку, насыщенности и компонентам светоносности.
ms.openlocfilehash: 55703239395c54beedf4b7383435253f9c37006f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420964"
---
# <a name="hsl-function"></a>Функция HSL

Возвращает значение, представляющее индекс в цветовой палитре документа. Он указывает цвет по своему оттенку, насыщенности и компонентам светоносности.
  
## <a name="syntax"></a>Синтаксис

HSL(** *hue* **, ** *saturation* **, ** *luminosity* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _hue_ <br/> |Обязательный  <br/> |**Number** <br/> |Оттенок цвета, выраженный как число в диапазоне от 0 до 239, включительно или выражение, которое оценивает до такого числа.  <br/> |
| _насыщение_ <br/> |Обязательный  <br/> |**Number** <br/> |Насыщенность цвета, выраженная как число в диапазоне от 0 до 240 включительно или выражение, оцениваемого до такого числа.  <br/> |
| _светоносность_ <br/> |Обязательный  <br/> |**Number** <br/> | Светоносность цвета, выраженная как число в диапазоне от 0 до 240 включительно или выражение, которое оценивается до такого числа.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Номер
  
## <a name="remarks"></a>Примечания

Если цвет, возвращенный функцией, еще не существует в цветовой палитре текущего документа, он добавляется в список доступных цветов документа. 
  
В следующей таблице перечислены некоторые стандартные цвета и их значения оттенка, насыщенности и светоустойкости. 
  
|**Color**|**Значение Hue**|**Значение насыщенности**|**Значение luminosity**|
|:-----|:-----|:-----|:-----|
|Черный  <br/> |0  <br/> |0  <br/> |24  <br/> |
|Синий  <br/> |160  <br/> |240  <br/> |120  <br/> |
|Зеленый  <br/> |80  <br/> |240  <br/> |120  <br/> |
|Cyan  <br/> |120  <br/> |240  <br/> |120  <br/> |
|Красный  <br/> |0  <br/> |240  <br/> |120  <br/> |
|Пурпурный  <br/> |200  <br/> |240  <br/> |120  <br/> |
|Желтый  <br/> |40  <br/> |240  <br/> |120  <br/> |
|Белый  <br/> |0  <br/> |0  <br/> |240  <br/> |
   
## <a name="example-1"></a>Пример 1

HSL (160 240 120)
  
Возвращает индекс для синего цвета.
  
## <a name="example-2"></a>Пример 2

HSL(HUE(FillForegnd), SAT (FillForegnd), MIN (LUM(FillForegnd)+100,240))
  
Возвращает индекс для цвета, зеркального цвета переднего плана заполнения с повышенной светоуядностью.
  

