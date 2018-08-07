---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Добавляет лица, указанного с помощью параметров emailAddresses и displayName как friend для пользователя при входе в социальных сетях.
ms.openlocfilehash: 2f4df9afc4c769cce0502792373702c1281fcad7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812759"
---
# <a name="isocialsession2followpersonex"></a>ISocialSession2::FollowPersonEx

Добавляет лица, указанного с помощью параметров _emailAddresses_ и _displayName_ как friend для пользователя при входе в социальных сетях. 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a>Параметры

_emailAddresses_
  
> [in] Массив, содержащий один или несколько допустимый SMTP-адреса для пользователя в социальных сетях.
    
_displayName_
  
> [in] Строка, содержащая отображаемое имя пользователя, добавляемого в качестве friend.
    
## <a name="remarks"></a>Замечания

Если Outlook Social Connector (OSC) обеспечивает более чем на SMTP-адрес в массиве с помощью параметра **emailAddresses** поставщика OSC можно предположить, что первый элемент является основной SMTP-адрес. 
  
Если поставщик установил элемент **followPerson** **значение true** в **возможности** XML, а ни один из элементов для _emailAddresses_ не соответствует пользователя в сети, поставщик должен возвращать ошибку OSC_E_NOT_FOUND. Если поставщик значение **followPerson** **значение false** в **возможности**, поставщик должен возвращать ошибку OSC_E_FAIL. 
  
При успешном применении метода **FollowPersonEx** поставщик может использовать строки с помощью параметра _displayName_ устранения человека в любой последующих friend подтверждения электронной почты, а не с адресом SMTP-адресов пользователя. С другой стороны поставщик должен быть обрабатывать OSC, передаче пустой строки для параметра _displayName_ . 
  
Если поставщик реализует интерфейс [ISocialSession2](isocialsession2iunknown.md) и установил **followPerson** как **true** в возможности XML, OSC вызывает **FollowPersonEx** вместо [ISocialSession::FollowPerson](isocialsession-followperson.md). Если поставщик **followPerson** задано **значение true** , но не реализует интерфейс **ISocialSession2** или **FollowPersonEx** возвращает OSC_E_NOTIMPL ошибка, OSC вызывает **ISocialSession::FollowPerson**.
  
## <a name="see-also"></a>См. также

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

