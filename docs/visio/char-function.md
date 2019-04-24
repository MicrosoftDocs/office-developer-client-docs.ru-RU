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
description: Возвращает символ ANSI для числа.
ms.openlocfilehash: 6f1c459892331ec30ad93bbc860fcd038e8f4732
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341911"
---
# <a name="char-function"></a>Функция CHAR

Возвращает символ ANSI для числа.
  
## <a name="syntax"></a>Синтаксис

CHAR (* * *Number* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _число_ <br/> |Обязательный  <br/> |**Number** <br/> |Число, символ ANSI которого вы хотите получить.  <br/> |
   
## <a name="remarks"></a>Комментарии

Результирующая строка — один символ в длину. Параметр _Number_ должен быть целым числом в диапазоне от 1 до 255 (включительно), иначе функция возвращает ошибку. 
  
## <a name="example"></a>Пример

CHAR (9) 
  
Возвращает знак табуляции. 
  

