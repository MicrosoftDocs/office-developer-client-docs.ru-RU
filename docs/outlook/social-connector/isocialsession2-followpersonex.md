---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Добавляет пользователя, идентифицированного по параметрам emailAddresses и displayName, в качестве друга во время входа пользователя в социальной сети.
ms.openlocfilehash: b44b442ba928b48411e5b1fc8a0c8b76477022ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429833"
---
# <a name="isocialsession2followpersonex"></a>ISocialSession2::FollowPersonEx

Добавляет пользователя, идентифицированного по  _параметрам emailAddresses_ и  _displayName,_ в качестве друга во время входа пользователя в социальной сети. 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a>Параметры

_emailAddresses_
  
> [in] Массив, содержащий один или несколько допустимых SMTP-адресов для человека в социальной сети.
    
_displayName_
  
> [in] Строка с отображаемой именем человека, добавляемого в качестве друга.
    
## <a name="remarks"></a>Примечания

Если Outlook Social Connector (OSC) предоставляет больше, чем smTP-адрес в массиве в параметре **emailAddresses,** поставщик OSC может предположить, что первый элемент является основным SMTP-адресом. 
  
Если поставщик установил для элемента **followPerson** в **XML** возможностей true и ни один из элементов _emailAddresses_ не соответствует пользователю в сети, поставщик должен вернуть OSC_E_NOT_FOUND ошибку.  Если поставщик установил **для followPerson в** возможностях false, поставщик должен вернуть OSC_E_FAIL ошибку.   
  
Если метод **FollowPersonEx** успешно используется, поставщик может использовать строку в параметре  _displayName_ для обращения к человеку в любом последующем сообщении электронной почты подтверждения друга, а не адресовать его по SMTP-адресу. С другой стороны, поставщик должен иметь возможность обрабатывать OSC, передав пустую строку для _параметра displayName._ 
  
Если поставщик реализует интерфейс [ISocialSession2](isocialsession2iunknown.md) и установил для  **followPerson** в XML возможностей true, OSC вызывает **FollowPersonEx** вместо [ISocialSession::FollowPerson](isocialsession-followperson.md). Если поставщик установил для **followPerson** true, но не реализует интерфейс **ISocialSession2** или **FollowPersonEx** возвращает ошибку OSC_E_NOTIMPL, OSC вызывает **ISocialSession::FollowPerson**. 
  
## <a name="see-also"></a>См. также

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

