---
title: Функция TRUNC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251508
localization_priority: Normal
ms.assetid: 62f074ef-5bf8-df1e-d826-fc1027a36501
description: Возвращает число, усеченное до указанного числа цифр.
ms.openlocfilehash: 5b2138ff3091f70313344d5b38d8225d572d8e70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426501"
---
# <a name="trunc-function"></a>Функция TRUNC

Возвращает число, усеченное до указанного числа цифр.
  
## <a name="syntax"></a>Синтаксис

TRUNC(** *number* **, ** *numberofdigits* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _число_ <br/> |Обязательна  <br/> |**Числовой** <br/> |Число для усечения.  <br/> |
| _numberofdigits_ <br/> |Обязательна  <br/> |**Числовой** <br/> |Количество цифр, к которым необходимо _усечено число._  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Числовая.
  
## <a name="remarks"></a>Примечания

Если _числоofdigits_ больше 0,  число усечено до _нумеруфайтов_ справа от десятичной замещений. Если  _numberofdigits_ имеет 0,  _число_ усечено до числа. Если  _числоofdigits_ меньше  _0,_ число усечено до  _нуфадигитов_ слева от десятичной заголовки. 
  
## <a name="example-1"></a>Пример 1

TRUNC(123.654,2)
  
Возвращает 123,65.
  
## <a name="example-2"></a>Пример 2

TRUNC(123.654,0)
  
Возвращает 123.
  
## <a name="example-3"></a>Пример 3

TRUNC(123.654,-1)
  
Возвращает 120.
  

