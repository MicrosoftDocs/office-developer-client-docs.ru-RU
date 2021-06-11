---
title: ISocialSessionLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b3c9a23-6378-4054-ad1c-193fc15c473c
description: Войдите на сайт социальной сети с помощью указанного имени пользователя и пароля.
ms.openlocfilehash: 7915097e456d6fafa713901f8074e6531bfaa001
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361042"
---
# <a name="isocialsessionlogon"></a>ISocialSession::Logon

Войдите на сайт социальной сети с помощью указанного имени пользователя и пароля.
  
```cpp
HRESULT _stdcall Logon([in] BSTR username, [in] BSTR password);
```

## <a name="parameters"></a>Parameters

_имя пользователя_
  
> [in] Строка, которая содержит имя пользователя для входа в систему.
    
_password_
  
> [in] Строка, в которую входит пароль для входа.
    
## <a name="see-also"></a>См. также

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

