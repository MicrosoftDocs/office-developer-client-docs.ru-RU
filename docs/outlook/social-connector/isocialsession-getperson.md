---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: Получает интерфейс ISocialPerson на основе параметра userID.
ms.openlocfilehash: b54e39b3712fb57d89d03787f1e5fa0ff50ff84a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439823"
---
# <a name="isocialsessiongetperson"></a>ISocialSession::GetPerson

Получает интерфейс [ISocialPerson](isocialpersoniunknown.md) на основе _параметра userID._ 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a>Параметры

_userId_
  
> [in] Строка, которая содержит ИД пользователя или SMTP-адрес пользователя.
    
_result_
  
> [out] Интерфейс **ISocialPerson.** 
    
## <a name="remarks"></a>Примечания

Параметр  _userID_ должен быть ид пользователя или SMTP-адрес. 
  
## <a name="see-also"></a>См. также

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

