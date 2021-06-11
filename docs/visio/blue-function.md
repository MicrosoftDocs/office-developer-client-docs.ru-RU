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
description: Возвращает синий компонент цвета. Возвращаемая величина — это набор в диапазоне от 0 до 255 включительно. Функция возвращает 0 для недействительных входных данных.
ms.openlocfilehash: adefbe0f8c2df0ead0f3e50cd5d4945501972865
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439039"
---
# <a name="blue-function"></a>Функция BLUE

Возвращает синий компонент цвета. Возвращаемая величина — это набор в диапазоне от 0 до 255 включительно. Функция возвращает 0 для недействительных входных данных.
  
## <a name="syntax"></a>Синтаксис

BLUE(** *expression* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Обязательный  <br/> |**String** <br/> |Индекс цвета в цветной таблице документа, выражение, которое решается на настраиваемый цвет (например, RGB или HSL), или ссылку на ячейку, содержаную цветной индекс или результат цвета.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Целое число
  
## <a name="example-1"></a>Пример 1

BLUE (Sheet.4! FillForegnd)
  
Возвращает синий компонент цвета поля заполняемого поля Sheet.4.
  
## <a name="example-2"></a>Пример 2

BLUE (13)
  
Возвращает 128, если в документе используется Visio цветовая палитра, где cyan — это цвет в индексе 13.
  
## <a name="example-3"></a>Пример 3

BLUE (RGB(10, 20, 30))
  
Возвращает 30.
  

