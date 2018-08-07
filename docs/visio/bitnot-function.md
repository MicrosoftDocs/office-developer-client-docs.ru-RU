---
title: Функция BITNOT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251399
localization_priority: Normal
ms.assetid: 7b6486bb-3618-3747-4b00-93bd55767c1c
description: Возвращает 16-разрядный двоичное число, в котором каждый бит равен 1 только в том случае, если соответствующий бит в двоичное число равняется 0. В противном случае бит равен 0.
ms.openlocfilehash: 0806e7c52cab659a09d27a60efb9c09aa436fb92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813225"
---
# <a name="bitnot-function"></a>Функция BITNOT

Возвращает 16-разрядный двоичное число, в котором каждый бит равен 1 только в том случае, если соответствующий бит в двоичное число равняется 0. В противном случае бит равен 0.
  
## <a name="syntax"></a>Синтаксис

BITNOT (** *двоичное число* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _двоичное число_ <br/> |Обязательный  <br/> |**Числовой** <br/> |16-разрядное двоичное число.  <br/> |
   
### <a name="return-value"></a>������������ ��������

16-разрядный двоичный
  
## <a name="example"></a>Пример

BITNOT(6)
  
Возвращает 65529. 6 = 0... 00110. Таким образом, BITNOT(6) = 1... 11001.
  

