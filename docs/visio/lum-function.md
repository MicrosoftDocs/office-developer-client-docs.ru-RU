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
description: Возвращает значение компонента luminosity цвета.
ms.openlocfilehash: 17fa43f8e2cd7422428f92724e351436233c2d62
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419340"
---
# <a name="lum-function"></a>Функция LUM

Возвращает значение компонента luminosity цвета.
  
## <a name="syntax"></a>Синтаксис

LUM(** *expression* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Обязательный  <br/> |**Числовой** <br/> |Индекс цвета в таблице цветов документа или ссылка на ячейку, содержаную индекс цвета.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Числовой
  
## <a name="remarks"></a>Примечания

Возвращаемая величина — это число в диапазоне от 0 до 240 включительно. Функция возвращает 0 для недопустимого ввода. 
  
## <a name="example-1"></a>Пример 1

LUM(Sheet.4! FillForegnd)
  
Возвращает luminosity цвета переднего плана заливки Sheet.4.
  
## <a name="example-2"></a>Пример 2

LUM(6)
  
Возвращает значение 120, если в документе используется цветовая палитра Visio по умолчанию, где magenta — это цвет в индексе 6.
  
## <a name="example-3"></a>Пример 3

LUM(HSL(10, 20, 30))
  
Возвращает 30.
  

