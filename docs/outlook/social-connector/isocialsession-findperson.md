---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Получает строку, представляюную одного или несколько пользователей, которые соответствуют параметру userID.
ms.openlocfilehash: 1aa6478126e509c8d707d6a8d11b2c8428177bbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434797"
---
# <a name="isocialsessionfindperson"></a>ISocialSession::FindPerson

Получает строку, представляюную одного или несколько пользователей, которые соответствуют _параметру userID._ 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a>Параметры

_userId_
  
> [in] ИД пользователя социальной сети, SMTP-адрес или отображаемого имени пользователя.
    
_result_
  
> [out] Строка XML, которая представляет одного или несколько человек, которые соответствуют идентификационным данным, указанным _параметром userId._ 
    
## <a name="remarks"></a>Примечания

Если запрос **FindPerson** соответствует одному или нескольким лицам, этот метод возвращает сведения о них в _параметре результата._ _Строка_ XML результата должна соответствовать определению схемы для друзей, как определено в схеме для возможности extensibility поставщика Outlook Social Connector (OSC).  
  
## <a name="see-also"></a>См. также

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

