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
description: 'Возвращает значение TRUE, если значение cellreference является типом #VALUE, где аргумент в формуле является неправильным типом. Функция ISERRVALUE используется в логических выражениях, которые ссылаются на другую ячейку.'
ms.openlocfilehash: 62058522dc8a2387aec9867e4892da740aba9b44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404430"
---
# <a name="iserrvalue-function"></a>Функция ISERRVALUE

Возвращает значение TRUE, если значение  _cellreference_ является типом #VALUE, где аргумент в формуле является неправильным типом. Функция ISERRVALUE используется в логических выражениях, которые ссылаются на другую ячейку. 
  
## <a name="syntax"></a>Синтаксис

ISERRVALUE(** *cellreference* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Обязательно  <br/> |**Строка** <br/> |Ссылка на ячейку.  <br/> |
   
## <a name="remarks"></a>Примечания

0000 ячеек A и D не возвращают #VALUE! ошибка, так как формула может содержать числа и буквы в одной строке. Ячейки X и Y должны содержать только числа. 
  
## <a name="example-1"></a>Пример 1

|**Cell**|**Formula**|**Возвращено значение**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |= "House"  <br/> |#ЗНАЧ!  <br/> |
|Scratch.A1  <br/> |= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)  <br/> |2   <br/> |
   
Возвращает 2, так как возвращаемая величина #VALUE! ошибка, и выражение предписывает Microsoft Visio вернуть 2, а не ошибку.
  
## <a name="example-2"></a>Пример 2

|**Cell**|**Formula**|**Возвращено значение**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |="5 + 7"  <br/> |5 + 7  <br/> |
|Scratch.B1  <br/> |=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)  <br/> |5 + 7  <br/> |
   
Возвращает 12, так как возвращаемая величина не является #VALUE! ошибка, и выражение предписывает Visio вернуть значение исходной ячейки.
  

