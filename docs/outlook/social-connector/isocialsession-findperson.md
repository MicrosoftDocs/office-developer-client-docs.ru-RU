---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Получает строку, представляющую одного или нескольких пользователей, соответствующих параметру идентификатор пользователя.
ms.openlocfilehash: 0b7525f853f7d97a991e2996a4e715cc53756d4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812737"
---
# <a name="isocialsessionfindperson"></a>ISocialSession::FindPerson

Получает строку, представляющую одного или нескольких пользователей, соответствующих параметру _идентификатор пользователя_ . 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a>Параметры

_userId_
  
> [in] Идентификатор пользователя социальных сетей, SMTP-адрес или отображаемое имя пользователя.
    
_результат_
  
> [out] XML-строка, которая представляет один или несколько пользователей, соответствующие данные идентификации, указанного с помощью параметра _идентификатор пользователя_ . 
    
## <a name="remarks"></a>Замечания

Если один или несколько лиц соответствует запрос **FindPerson** , этот метод возвращает сведения для пользователей с помощью параметра _результатов_ . XML-строка _результат_ должен соответствовать требованиям определение схемы для **друзей**, определенных в схеме для расширений поставщика Outlook Social Connector (OSC). 
  
## <a name="see-also"></a>См. также

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

