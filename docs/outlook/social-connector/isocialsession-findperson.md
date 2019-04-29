---
title: ИсоЦиалсессионфиндперсон
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Получает строку, представляющую одного или нескольких лиц, которые совпадают с параметром userID.
ms.openlocfilehash: 1aa6478126e509c8d707d6a8d11b2c8428177bbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434797"
---
# <a name="isocialsessionfindperson"></a>ISocialSession::FindPerson

Получает строку, представляющую одного или нескольких лиц, которые совпадают с параметром _UserID_ . 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a>Параметры

_userId_
  
> возврата Идентификатор пользователя социальной сети, SMTP-адрес или отображаемое имя пользователя.
    
_result_
  
> вышли XML-строка, представляющая одного или нескольких лиц, которые совпадают с идентификационными данными, указанными в параметре _UserID_ . 
    
## <a name="remarks"></a>Примечания

Если один или несколько пользователей соответствуют запросу **финдперсон** , этот метод возвращает сведения об этих лицах в параметре _result_ . _Результирующая_ XML-строка должна соответствовать определению схемы для **друзей**, как определено в схеме Расширяемость поставщика Outlook Social Connector (OSC). 
  
## <a name="see-also"></a>См. также

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

