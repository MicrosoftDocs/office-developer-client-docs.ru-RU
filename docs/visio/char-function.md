---
title: Функция CHAR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251406
localization_priority: Normal
ms.assetid: 0803d5d3-d804-5ffe-604d-661b35d1fc01
description: Возвращает для числа символов ANSI.
ms.openlocfilehash: 209614d20dd663ed2f7ca030c25500d43f925c95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813364"
---
# <a name="char-function"></a>Функция CHAR

Возвращает для числа символов ANSI.
  
## <a name="syntax"></a>Синтаксис

ЗНАКОВ (** *номер* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Обязательный  <br/> |**Число** <br/> |Номер, чтобы получить символ ANSI.  <br/> |
   
## <a name="remarks"></a>Замечания

Результирующую строку — один символ. Параметр _номер_ должно быть целое число от 1 до 255 (включительно) или функция возвращает ошибку. 
  
## <a name="example"></a>Пример

CHAR(9) 
  
Возвращает символ табуляции. 
  

