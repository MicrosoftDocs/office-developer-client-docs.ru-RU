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
description: Возвращает имя листа в качестве строки.
ms.openlocfilehash: 7d0a4e9f3c5f70be07e9cc5691f52afcbc7bea68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416799"
---
# <a name="name-function"></a>Функция NAME

Возвращает имя листа в качестве строки.
  
## <a name="syntax"></a>Синтаксис

NAME (** *langID_opt* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Необязательна  <br/> |**Number** <br/> |Используется для указания языка для строки, возвращаемой функцией. Используйте 0 (значение по умолчанию) для указания локального языка. Используйте 750 для указания универсального языка.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

String
  
## <a name="remarks"></a>Примечания

Если вы передаете запрещенный код языка, используется локальный язык. 
  

