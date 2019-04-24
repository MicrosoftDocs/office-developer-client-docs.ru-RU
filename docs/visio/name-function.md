---
title: Функция NAME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251580
localization_priority: Normal
ms.assetid: 1ca67a09-9df2-37f5-b269-e761d76bb011
description: Возвращает имя листа в виде строки.
ms.openlocfilehash: 7d0a4e9f3c5f70be07e9cc5691f52afcbc7bea68
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319427"
---
# <a name="name-function"></a>Функция NAME

Возвращает имя листа в виде строки.
  
## <a name="syntax"></a>Синтаксис

ИМЯ (* * *лангид_опт* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _Лангид_опт_ <br/> |Необязательный  <br/> |**Number** <br/> |Используется для указания языка для строки, которую возвращает функция. Используйте значение 0 (значение по умолчанию), чтобы указать локальный язык. Используйте 750, чтобы указать универсальный язык.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Строка
  
## <a name="remarks"></a>Замечания

Если вы передаете недопустимый код языка, используется локальный язык. 
  

