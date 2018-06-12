---
title: Функция Яркость
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251460
localization_priority: Normal
ms.assetid: 38e6bba7-1bf2-3d31-0912-707002454f5d
description: Возвращает значение компонента яркости цвета.
ms.openlocfilehash: 9c9594aff0149a54d7faacdf8295e6c214c43348
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814187"
---
# <a name="lum-function"></a>Функция Яркость

Возвращает значение компонента яркости цвета.
  
## <a name="syntax"></a>Синтаксис

Яркость (** *выражение* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Обязательный  <br/> |**Числовой** <br/> |Индекс цвета в таблице цветов документа или ссылка на ячейку, которая содержит индекс цвета.  <br/> |
   
### <a name="return-value"></a>������������ ��������

Число
  
## <a name="remarks"></a>Замечания

Возвращаемое значение — число в диапазоне от 0 до 240 включительно. Функция возвращает 0 для недопустимые данные. 
  
## <a name="example-1"></a>Пример 1

Яркость (Sheet.4! FillForegnd)
  
Возвращает яркость цвет заливки Sheet. 4.
  
## <a name="example-2"></a>Пример 2

LUM(6)
  
Возвращает 120, если в документе используется по умолчанию Visio цветовой палитры, в котором пурпурный цвет по индексу 6.
  
## <a name="example-3"></a>Пример 3

ЯРКОСТЬ (HSL (10, 20, 30))
  
Возвращает 30.
  

