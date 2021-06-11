---
title: Функция STRSAME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251786
localization_priority: Normal
ms.assetid: d9fc2007-cc21-b20c-adee-be87cc356753
description: Определяет, являются ли строки одинаковыми. Он возвращает TRUE, если они одинаковы и FALSE, если они не являются.
ms.openlocfilehash: 0f298c966ec7a3f1e23c89473fecc555ed950f79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428685"
---
# <a name="strsame-function"></a>Функция STRSAME

Определяет, являются ли строки одинаковыми. Он возвращает TRUE, если они одинаковы и FALSE, если они не являются. 
  
## <a name="syntax"></a>Синтаксис

STRSAME (" ** *string1* ** ", " ** *string2* ** ", ** *ignoreCase* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _строка1_ <br/> |Обязательный  <br/> |**String** <br/> |Первая строка для сравнения.  <br/> |
| _строка2_ <br/> |Обязательный  <br/> |**String** <br/> |Вторая строка для сравнения.  <br/> |
| _ignoreCase_ <br/> |Необязательный  <br/> |**Логический** <br/> |TRUE, чтобы игнорировать случай и FALSE, чтобы сравнить случай. По умолчанию значение FALSE.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Boolean
  
## <a name="remarks"></a>Примечания

Чтобы сравнить строки с несколькими байтами или сделать сравнения с использованием правил дела для определенного локального, используйте функцию STRSAMEEX.
  
## <a name="example-1"></a>Пример 1

STRSAME ("cat", "dog")
  
Возвращает FALSE.
  
## <a name="example-2"></a>Пример 2

STRSAME ("cat", "cat")
  
Возвращает TRUE.
  
## <a name="example-3"></a>Пример 3

STRSAME ("cat", "cat", TRUE)
  
Возвращает TRUE.
  
## <a name="example-4"></a>Пример 4

STRSAME ("cat", "CAT")
  
Возвращает FALSE.
  
## <a name="example-5"></a>Пример 5

STRSAME ("cat", "CAT", TRUE)
  
Возвращает TRUE.
  
## <a name="example-6"></a>Пример 6

STRSAME ("cät", "CAT", TRUE)
  
Возвращает FALSE.
  
## <a name="example-7"></a>Пример 7

STRSAME ("cät", "CÄT", TRUE)
  
Возвращает TRUE.
  

