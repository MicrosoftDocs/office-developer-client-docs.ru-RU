---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Добавляет пользователя, идентифицированного по параметрам emailAddresses и displayName в качестве друга для зарегистрированного пользователя в социальной сети.
ms.openlocfilehash: b44b442ba928b48411e5b1fc8a0c8b76477022ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429833"
---
# <a name="isocialsession2followpersonex"></a>ISocialSession2::FollowPersonEx

Добавляет пользователя, идентифицированного по  _параметрам emailAddresses_ и  _displayName_ в качестве друга для зарегистрированного пользователя в социальной сети. 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a>Parameters

_emailAddresses_
  
> [in] Массив, содержащий один или несколько действительных SMTP-адресов для человека в социальной сети.
    
_displayName_
  
> [in] Строка с отображаемой именем человека, который будет добавлен в качестве друга.
    
## <a name="remarks"></a>Примечания

Если Outlook social Connector (OSC) предоставляет больше, чем на SMTP-адресе в массиве в параметре **emailAddresses,** поставщик OSC может предположить, что первым элементом является основной SMTP-адрес. 
  
Если поставщик установил элемент **followPerson** как  верный в XML-возможностях, и ни один из элементов _для emailAddresses_ не соответствует пользователю в сети, поставщик должен вернуть OSC_E_NOT_FOUND ошибку.  Если поставщик установил **followPerson** как ложный в возможностях, поставщик должен вернуть OSC_E_FAIL ошибку.   
  
Если метод **FollowPersonEx** успешно используется, поставщик может использовать строку в параметре  _displayName_ для адресов пользователя в любом последующем электронном сообщении подтверждения друга, а не адресовать его по smTP-адресу. С другой стороны, поставщик должен иметь возможность обрабатывать osC, передав пустую строку для _параметра displayName._ 
  
Если поставщик реализует [интерфейс ISocialSession2](isocialsession2iunknown.md) и установил **followPerson** как верный в возможностях XML, OSC вызывает **FollowPersonEx** вместо [ISocialSession::FollowPerson](isocialsession-followperson.md).  Если поставщик установил **followPerson** как true, но не реализует интерфейс **ISocialSession2** или **FollowPersonEx** возвращает ошибку OSC_E_NOTIMPL, OSC вызывает **ISocialSession::FollowPerson**. 
  
## <a name="see-also"></a>См. также

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

