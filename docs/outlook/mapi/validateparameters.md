---
title: ValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParameters
api_type:
- COM
ms.assetid: 80aadd11-5409-4636-8fad-fa2206336671
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b3862ea539907bb0570a0e845b09a15e7bed0507
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425205"
---
# <a name="validateparameters"></a>ValidateParameters

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Вызывает внутреннюю функцию для проверки параметров, которые клиентские приложения передали поставщикам услуг. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг  <br/> |
   
```cpp
HRESULT ValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Параметры

 _eMethod_
  
> [in] Указывает путем переумерия метод проверки. 
    
 _First_
  
> [in] Указатель на первый аргумент в стеке.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Все параметры действительны. 
    
MAPI_E_CALL_FAILED 
  
> Один или несколько параметров не допустимы.
    
## <a name="remarks"></a>Примечания

Макрос **ValidateParameters** был сменяем макрос [ValidateParms.](validateparms.md) **ValidateParameters** не работает правильно на платформах RISC и теперь не позволяет компиляции на них. Он по-прежнему компиляции и работает правильно на платформах Intel, но **ValidateParms** рекомендуется на всех платформах. 
  

