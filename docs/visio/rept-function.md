---
title: Функция REPT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027335
localization_priority: Normal
ms.assetid: 53362a32-ac27-42a3-ace1-c6184ab20b52
description: Повторяет текст заданное количество раз.
ms.openlocfilehash: 84e7167fcee426c607e6967aff0530362685dd35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412081"
---
# <a name="rept-function"></a>Функция REPT

Повторяет текст заданное количество раз. 
  
## <a name="syntax"></a>Синтаксис

REPT (** *text* **, ** *number_times* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Обязательно  <br/> |**Строка** <br/> | Текст, который нужно повторить.  <br/> |
| _number_times_ <br/> |Обязательна  <br/> |**Number** <br/> |Положительное число, определяющие количество повторов текста.  <br/> |
   
## <a name="remarks"></a>Примечания

Если *number_times:* 
  
- Ноль (0), REPT возвращает "" (пустой текст).
    
- Не является межуголным, оно усечено.
    
## <a name="example"></a>Пример

REPT (" \* ", 5) 
  
Возвращает \* \* \* \* \* . 
  

