---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Получает строку, представляюную одного или несколько лиц, которые соответствуют параметру userID.
ms.openlocfilehash: 1aa6478126e509c8d707d6a8d11b2c8428177bbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434797"
---
# <a name="isocialsessionfindperson"></a>ISocialSession::FindPerson

Получает строку, представляюную одного или несколько лиц, которые соответствуют _параметру userID._ 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a>Parameters

_userId_
  
> [in] ID пользователя социальной сети, SMTP-адрес или отображение имени пользователя.
    
_result_
  
> [вышел] Строка XML, которая представляет одного или несколько лиц, которые соответствуют данным идентификации, указанным _параметром userId._ 
    
## <a name="remarks"></a>Примечания

Если один или несколько лиц соответствуют запросу **FindPerson,** этот метод возвращает сведения для этих лиц в _параметре результат._ _Строка_ XML должна соответствовать определению схемы для друзей, как определено в схеме для Outlook поставщика социальных соединителем (OSC).  
  
## <a name="see-also"></a>См. также

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

