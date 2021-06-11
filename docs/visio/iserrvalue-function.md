---
title: Функция ISERRVALUE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251453
localization_priority: Normal
ms.assetid: c7feec6f-f47a-60ee-b056-7b2dc51ed9a9
description: 'Возвращает ЗНАЧЕНИЕ TRUE, если значение cellreference — тип #VALUE, если аргумент в формуле неправильный. Функция ISERRVALUE используется в логических выражениях, которые относятся к другой ячейке.'
ms.openlocfilehash: 62058522dc8a2387aec9867e4892da740aba9b44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404430"
---
# <a name="iserrvalue-function"></a>Функция ISERRVALUE

Возвращает ЗНАЧЕНИЕ TRUE, если значение  _cellreference_ — тип #VALUE, если аргумент в формуле неправильный. Функция ISERRVALUE используется в логических выражениях, которые относятся к другой ячейке. 
  
## <a name="syntax"></a>Синтаксис

ISERRVALUE(** *cellreference* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Обязательный  <br/> |**String** <br/> |Ссылка на ячейку.  <br/> |
   
## <a name="remarks"></a>Примечания

Scratch cells A through D won't return a #VALUE! ошибка, так как формула может содержать цифры и буквы в одной строке. Ячейки X и Y должны содержать только числа. 
  
## <a name="example-1"></a>Пример 1

|**Cell**|**Формула**|**Возвращено значение**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |= "Дом"  <br/> |#ЗНАЧ!  <br/> |
|Scratch.A1  <br/> |= Если (ISERRVALUE(Scratch.X1),2,Scratch.X1)  <br/> |2  <br/> |
   
Возвращает 2, так как возвращенные значения #VALUE! ошибка, и выражение предписывает корпорации Майкрософт Visio вернуть 2 на место ошибки.
  
## <a name="example-2"></a>Пример 2

|**Cell**|**Формула**|**Возвращено значение**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |="5 + 7"  <br/> |5 + 7  <br/> |
|Scratch.B1  <br/> |=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)  <br/> |5 + 7  <br/> |
   
Возвращает 12, так как возвращенные значения не являются #VALUE! ошибка, и выражение Visio вернуть значение исходной ячейки.
  

