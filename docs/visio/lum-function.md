---
title: Функция LUM
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251460
localization_priority: Normal
ms.assetid: 38e6bba7-1bf2-3d31-0912-707002454f5d
description: Возвращает значение компонента яркости цвета.
ms.openlocfilehash: 17fa43f8e2cd7422428f92724e351436233c2d62
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419340"
---
# <a name="lum-function"></a>Функция LUM

Возвращает значение компонента яркости цвета.
  
## <a name="syntax"></a>Синтаксис

ЯРКОСТЬ (* * *Expression* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Обязательный  <br/> |**Числовой** <br/> |Индекс цвета в таблице цветов документа или ссылка на ячейку, содержащую цветовой индекс.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Номер
  
## <a name="remarks"></a>Примечания

Возвращаемое значение — число в диапазоне от 0 до 240 включительно. Функция возвращает значение 0 для недопустимых входных данных. 
  
## <a name="example-1"></a>Пример 1

ЯРКОСТЬ (sheet. 4! FillForegnd
  
Возвращает яркость листа. 4's заливки текста.
  
## <a name="example-2"></a>Пример 2

ЯРКОСТЬ (6)
  
Возвращает 120, если документ использует цветовую палитру Visio по умолчанию, где пурпурный — цвет с индексом 6.
  
## <a name="example-3"></a>Пример 3

ЯРКОСТЬ (HSL (10, 20, 30))
  
Возвращает значение 30.
  

