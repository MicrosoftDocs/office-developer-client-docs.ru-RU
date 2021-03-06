---
title: UlValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParameters
api_type:
- COM
ms.assetid: fb9050c9-5797-44f0-8bf5-6264f4e6d7c3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 465069f08e2026dcbf98e24f0f5f59e12ed17eca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431276"
---
# <a name="ulvalidateparameters"></a>UlValidateParameters

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Вызывает внутреннюю функцию проверки параметров, которые клиентские приложения передали поставщикам услуг и MAPI. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг  <br/> |
   
```cpp
HRESULT UlValidateParameters(
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
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_E_CALL_FAILED 
  
> Ошибка неожиданного или неизвестного происхождения не позволяет завершить операцию.
    
## <a name="remarks"></a>Примечания

Макрос **UlValidateParameters** был вытеснен [макросом UlValidateParms.](ulvalidateparms.md) **UlValidateParameters** не работает правильно на платформах RISC и теперь не позволяет компиляции на них. Он по-прежнему правильно компилирует и работает на платформах Intel, но **рекомендуется использовать UlValidateParms** на всех платформах. 
  

