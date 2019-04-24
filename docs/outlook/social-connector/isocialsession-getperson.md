---
title: ИсоЦиалсессионжетперсон
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: Получает интерфейс ИсоЦиалперсон, основанный на параметре userID.
ms.openlocfilehash: b54e39b3712fb57d89d03787f1e5fa0ff50ff84a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285332"
---
# <a name="isocialsessiongetperson"></a>ISocialSession::GetPerson

Получает интерфейс [исоЦиалперсон](isocialpersoniunknown.md) , основанный на параметре _UserID_ . 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a>Параметры

_userId_
  
> возврата Строка, содержащая идентификатор пользователя или SMTP-адрес человека.
    
_result_
  
> вышли Интерфейс **исоЦиалперсон** . 
    
## <a name="remarks"></a>Замечания

Параметр _UserID_ должен быть идентификатором пользователя или SMTP-адресом. 
  
## <a name="see-also"></a>См. также

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

