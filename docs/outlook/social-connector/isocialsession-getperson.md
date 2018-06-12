---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: Получает интерфейс ISocialPerson на основе параметра идентификатор пользователя.
ms.openlocfilehash: 5769f4c41bb97f45ab722f1b3a3febe24c8a7ab2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812739"
---
# <a name="isocialsessiongetperson"></a>ISocialSession::GetPerson

Получает интерфейс [ISocialPerson](isocialpersoniunknown.md) на основе параметра _идентификатор пользователя_ . 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a>Parameters

_userId_
  
> [in] Строка, содержащая пользователя ID или адрес SMTP пользователя.
    
_результат_
  
> [out] Интерфейс **ISocialPerson** . 
    
## <a name="remarks"></a>Замечания

Параметр _идентификатор пользователя_ должен быть адрес SMTP или идентификатор пользователя. 
  
## <a name="see-also"></a>См. также

- [ISocialSession: IUnknown](isocialsessioniunknown.md)

