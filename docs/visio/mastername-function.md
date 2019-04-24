---
title: Функция MASTERNAME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251581
localization_priority: Normal
ms.assetid: 519d79d4-9178-2231-c26d-aa7f31a43412
description: Возвращает имя образца листа в виде строки или возвращает строку "No Master", если у листа нет образца.
ms.openlocfilehash: 7732cf9e8b23e2fd0fc2e3f2cc8d9ef4f39fd67f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341799"
---
# <a name="mastername-function"></a>Функция MASTERNAME

Возвращает имя образца листа в виде строки или возвращает строку "\<без образца\>", если у листа нет образца.
  
## <a name="syntax"></a>Синтаксис

MASTERNAME ([* * *лангид_опт* * *]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _Лангид_опт_ <br/> |Необязательно заполнять.  <br/> |**Number** <br/> |Используется для указания языка для строки, которую возвращает функция. Используйте значение 0 (значение по умолчанию), чтобы указать локальный язык. Используйте 750, чтобы указать универсальный язык.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Строка
  
## <a name="remarks"></a>Комментарии

Если вы передаете недопустимый код языка, используется локальный язык. 
  

