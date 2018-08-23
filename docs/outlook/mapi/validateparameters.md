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
ms.openlocfilehash: 662330a7b8c665471e9bbe6af27dff84ee68c8cf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586069"
---
# <a name="validateparameters"></a>ValidateParameters

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Вызывает функцию внутреннего и проверять параметры клиентских приложений не имеет разрешений для поставщиков услуг. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Поставщики услуг  <br/> |
   
```cpp
HRESULT ValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Параметры

 _eMethod_
  
> [in] Указывает перечисление, метод для проверки. 
    
 _Первый_
  
> [in] Указатель на первый аргумент в стеке.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Все параметры являются допустимыми. 
    
MAPI_E_CALL_FAILED 
  
> Один или несколько параметров являются недопустимыми.
    
## <a name="remarks"></a>Замечания

Макрос **ValidateParameters** был заменен макрос [ValidateParms](validateparms.md) . **ValidateParameters** не работает на платформах RISC и теперь запрещено компиляцию на них. По-прежнему компилирует и работает правильно на платформах, но **ValidateParms** рекомендуется для всех платформ. 
  

