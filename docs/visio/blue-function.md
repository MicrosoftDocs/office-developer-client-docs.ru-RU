---
title: Функция BLUE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251402
localization_priority: Normal
ms.assetid: da9fb933-4e2c-3e2a-1879-6e70db0cd830
description: Возвращает синий компонент цвета. Возвращаемая величина — это целый ряд в диапазоне от 0 до 255 включительно. Функция возвращает 0 для недопустимого ввода.
ms.openlocfilehash: adefbe0f8c2df0ead0f3e50cd5d4945501972865
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439039"
---
# <a name="blue-function"></a>Функция BLUE

Возвращает синий компонент цвета. Возвращаемая величина — это целый ряд в диапазоне от 0 до 255 включительно. Функция возвращает 0 для недопустимого ввода.
  
## <a name="syntax"></a>Синтаксис

BLUE(** *expression* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Обязательно  <br/> |**Строка** <br/> |Индекс цвета в таблице цветов документа, выражение, которое соеется с пользовательским цветом (например, RGB или HSL) или ссылку на ячейку, которая содержит индекс цвета или результат цвета.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Целое число
  
## <a name="example-1"></a>Пример 1

BLUE(Sheet.4! FillForegnd)
  
Возвращает синий компонент цвета переднего плана заливки Sheet.4.
  
## <a name="example-2"></a>Пример 2

BLUE(13)
  
Возвращает значение 128, если документ использует цветовую палитру Visio по умолчанию, где cyan — это цвет в индексе 13.
  
## <a name="example-3"></a>Пример 3

BLUE(RGB(10, 20, 30))
  
Возвращает 30.
  

